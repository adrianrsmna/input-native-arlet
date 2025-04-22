# LoginApp
package com.example.loginapp;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    private EditText usernameField, passwordField;
    private Button loginButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        usernameField = findViewById(R.id.username);
        passwordField = findViewById(R.id.password);
        loginButton   = findViewById(R.id.loginButton);

        loginButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String user = usernameField.getText().toString();
                String pass = passwordField.getText().toString();

                if (user.equals("admin") && pass.equals("1234")) {
                    Toast.makeText(MainActivity.this, "Login Berhasil", Toast.LENGTH_SHORT).show();
                    // Tambahkan intent ke activity berikutnya jika diperlukan
                } else {
                    Toast.makeText(MainActivity.this, "Username atau Password salah", Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}

##Error
![Screenshot (568)](https://github.com/user-attachments/assets/d7a1d149-1f71-4b52-9e27-8ad6d6e6736b)



