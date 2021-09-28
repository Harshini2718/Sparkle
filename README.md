package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.ImageView;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    private ImageView Logo;
    private EditText Name;
    private EditText Password;
    private Button Login;
    private int counter=5;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ImageView Logo = findViewById(R.id.imageView2);
        EditText Name = findViewById(R.id.editTextTextPersonName2);
        EditText Password = findViewById(R.id.editTextTextPassword);
        Button Login = findViewById(R.id.Login);

        Login.setOnClickListener(view -> validate(Name.getText().toString(),Password.getText().toString()));
    }
    private void validate(String Username,String Userpassword){
        if((Username.equals("Admin")) && (Userpassword.equals("1111"))){
            Intent intent = new Intent (MainActivity.this,Sparkleactivity3.class);
            startActivity(intent);
        }else{
            counter--;

            if(counter == 0) {
                Login.setEnabled(false);

            }
        }
    }
}

package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Button;

public class Sparkleactivity3 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sparkleactivity3);
        Intent intent = new Intent (Sparkleactivity3.this,SparkleActivity4.class);
        startActivity(intent);
    }
}

package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class SparkleActivity4 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sparkle4);
        Intent intent = new Intent (SparkleActivity4.this,SparkleActivity5.class);
        startActivity(intent);
    }
}

package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class SparkleActivity5 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sparkle5);
        Intent intent = new Intent (SparkleActivity5.this,SparkleActivity6.class);
        startActivity(intent);
    }
}

package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class SparkleActivity6 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sparkle6);
        Intent intent = new Intent (SparkleActivity6.this,SparkleActivity7.class);
        startActivity(intent);
    }
}


@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_sparkle6);
    Intent intent = new Intent (SparkleActivity7.this,SparkleActivity.class);
    startActivity(intent);
}

package com.sparkle.app;

import android.content.Intent;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;

public class SparkleActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_sparkleactivity);
    }
}

