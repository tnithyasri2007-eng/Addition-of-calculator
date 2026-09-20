# Addition-of-calculator
## Name : Nithyasri T
## Register Number: 212225220068
## AIM

To create an Android application using **Android Studio** to get two numbers from the user and display their **summation value** in a text box.

## APPARATUS REQUIRED

* Computer/Laptop
* Android Studio
* Android SDK
* JDK (Java Development Kit)
* Android Emulator or Android Mobile Device
* Internet connection for initial setup

## PROCEDURE

1. Open **Android Studio** and create a new Android project.
2. Select **Empty Views Activity** and create the project.
3. Open `activity_main.xml`.
4. Design the user interface using **ConstraintLayout**.
5. Add two `EditText` fields to enter the first and second numbers.
6. Add a `Button` with the text **ADD**.
7. Add an `EditText` to display the summation value.
8. Open `MainActivity.java`.
9. Initialize the `EditText` and `Button` using `findViewById()`.
10. Set an `OnClickListener` for the ADD button.
11. Read the two numbers entered by the user.
12. Convert the input values into numeric values.
13. Add the two numbers and store the result.
14. Display the calculated summation value in the result text box.
15. Run the application using the Android Emulator or a connected Android device.
16. Enter two numbers and click the **ADD** button.
17. Verify that the correct summation value is displayed.

## PROGRAM
```
/*
Program to create and design an android application that Adds two numbers.
Developed by:RACHITHA U
Registeration Number :212225220078
*/
```
activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Addition of Two Numbers"
        android:textSize="24sp"
        android:textStyle="bold"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="50dp"/>

    <EditText
        android:id="@+id/num1"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal"
        app:layout_constraintTop_toBottomOf="@id/title"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="40dp"/>

    <EditText
        android:id="@+id/num2"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal"
        app:layout_constraintTop_toBottomOf="@id/num1"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="20dp"/>

    <Button
        android:id="@+id/addButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="ADD"
        app:layout_constraintTop_toBottomOf="@id/num2"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="30dp"/>

    <EditText
        android:id="@+id/result"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:hint="Summation Value"
        android:inputType="numberDecimal"
        android:focusable="false"
        app:layout_constraintTop_toBottomOf="@id/addButton"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="30dp"/>

</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivity.java:
```
package com.example.add;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {
    EditText num1, num2, result;
    Button addButton;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        result = findViewById(R.id.result);
        addButton = findViewById(R.id.addButton);

        addButton.setOnClickListener(v -> {
            double a = Double.parseDouble(num1.getText().toString());
            double b = Double.parseDouble(num2.getText().toString());

            double sum = a + b;

            result.setText(String.valueOf(sum));
        });
    }
}
```
## OUTPUT
<img width="1920" height="1080" alt="Screenshot 2026-09-20 170115" src="https://github.com/user-attachments/assets/1d51bc12-c617-4913-a163-b36735d5857e" />


## RESULT

Thus, an Android application for **addition of two numbers** was successfully created using **Android Studio and ConstraintLayout**. The application accepts two numbers from the user and successfully displays their **summation value** in the result text box.
