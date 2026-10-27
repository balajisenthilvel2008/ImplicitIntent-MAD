# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “https://mail.gmail.com ” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. Start the program.
2. Create an Android application using Android Studio.
3. Design the user interface with an `EditText` field to enter the website URL and a **Navigate** button.
4. Initialize the `EditText` and `Button` components in the `MainActivity.java` file.
5. Set an `OnClickListener` for the Navigate button.
6. Retrieve the URL entered by the user from the text field.
7. Create an implicit intent using `Intent.ACTION_VIEW` and `Uri.parse(url)`.
8. Call `startActivity(intent)` to open the specified URL in a suitable application or web browser.
9. Run the application and enter `https://mail.gmail.com` in the text field.
10. Click the **Navigate** button to open the Gmail page.
11. Stop the program.



## PROGRAM:
```
/*
Program to implement “Implicitintent”.
Developed by: Balaji S
Registration Number : 212225220015
*/
```

### MainActivity.java

```java
package com.example.demo;

import android.os.Bundle;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText editText=(EditText) findViewById(R.id.editText);
        Button button=findViewById(R.id.btn);
        button.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View view){
                String url=editText.getText().toString();
                Intent intent=new Intent(Intent.ACTION_VIEW,Uri.parse(url));
                startActivity(intent);
            }
        });

    }
}
```

### activity_main.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#E046B3"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="24dp"
        android:fontFamily="sans-serif-smallcaps"
        android:text="Exp 2a Implicit Intent"
        android:textColor="#00FFDC"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/editText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.177" />

    <EditText
        android:id="@+id/editText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="64dp"
        android:ems="10"
        android:inputType="text"
        app:layout_constraintBottom_toTopOf="@+id/btn"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/btn"
        style="@style/Widget.AppCompat.Button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="332dp"
        android:text="Navigate"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.554"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="serif"
        android:text="Enter Website"
        android:textColor="#09E9C4"
        android:textSize="22sp"
        app:layout_constraintBottom_toTopOf="@+id/editText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.503" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## OUTPUT
<img width="1920" height="1020" alt="Screenshot 2026-10-27 062015" src="https://github.com/user-attachments/assets/aefbe58d-598a-4f3d-bafd-5d9e01646e19" />
<br>
<img width="1920" height="1020" alt="Screenshot 2026-10-27 062353" src="https://github.com/user-attachments/assets/24af9b45-543c-4a3e-b605-85911419dc41" />
<br>
<img width="1920" height="1020" alt="Screenshot 2026-10-27 062643" src="https://github.com/user-attachments/assets/37763898-0525-47b6-8fda-f9db295fc36e" />

## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


