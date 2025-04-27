## input native & arlet
Nama = Adrian Rusmana
Kelas = TIF-RP23 CNS C
NPM = 23552011228



## Activity_Main
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="24dp">

    <EditText
        android:id="@+id/editTextInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Masukkan sesuatu" />

    <Button
        android:id="@+id/buttonSubmit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Tampilkan Alert"
        android:layout_marginTop="16dp" />
</LinearLayout>

## MainActivity

package com.example.inputalert

import android.os.Bundle
import android.util.Log
import android.widget.Button
import android.widget.EditText
import android.widget.Toast
import androidx.appcompat.app.AlertDialog
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {

    private lateinit var editTextInput: EditText
    private lateinit var buttonSubmit: Button

    companion object {
        private const val TAG = "MainActivity"
    }

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        editTextInput = findViewById(R.id.editTextInput)
        buttonSubmit = findViewById(R.id.buttonSubmit)

        buttonSubmit.setOnClickListener {
            val input = editTextInput.text.toString()

            // Tambahkan Log
            Log.d(TAG, "User Input: $input")

            // Tambahkan Toast
            Toast.makeText(this, "Input: $input", Toast.LENGTH_SHORT).show()

            // Tampilkan AlertDialog
            showAlert(input)
        }
    }

    private fun showAlert(message: String) {
        AlertDialog.Builder(this)
            .setTitle("Inputan Kamu")
            .setMessage(message)
            .setPositiveButton("OK", null)
            .show()
    }
}

## run

![Screenshot (315)](https://github.com/user-attachments/assets/0266a70e-4b7e-451a-a44e-251dce4b29f7)

![WhatsApp Image 2025-04-27 at 19 47 09_76450b28](https://github.com/user-attachments/assets/db9e6ec9-f2be-4335-b0da-bd1ea742ac74)

![WhatsApp Image 2025-04-27 at 19 47 09_1cc64c89](https://github.com/user-attachments/assets/ff42e557-dd66-46b2-a306-eb6e4b62f1f4)





