# HOW TO CREATE ANDROID PROJECT

### Create a project: File > New > New Project

![img.png](img/img.png)

### Choose the kind of activity: Choose "New Views Activity"

![img_1.png](img/img_1.png)

### Project Setting: Set *Name*, *Language* to `Java`, *Minimum

SDK* to `API 24: Android 7.0 (Nougat)`

![img_2.png](img/img_2.png)

### Project Structure

Layout will be defined in `res` > `layout`

![img_4.png](img_4.png)

To create the layout, start modify code in `activity_main.xml`

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent"
    android:layout_height="match_parent" tools:context=".MainActivity">

    <TextView android:id="@+id/helloWorldText" android:layout_width="wrap_content"
        android:layout_height="wrap_content" android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent" app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

The layout can be set to 3 options

`Code Only`

![img_5.png](img_5.png)

`Spilt`

![img_6.png](img_6.png)

`Design Only`

![img_7.png](img_7.png)

### Java Code: Include the following code in `MainActivity.java` to create the first Android App

```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Get a reference to the GUI
        TextView helloWorld = (TextView) findViewById(R.id.helloWorldText);

        // Generate a random number from 0 - 100
        int mark = 0;
        Random r = new Random();
        mark = r.nextInt(100);
        mark++;

        // Output the result
        helloWorld.setTextSize(30);
        helloWorld.setTextColor(Color.BLUE);
        helloWorld.setText("Hello World !\n");
        helloWorld.append("Your mark is: " + mark);

        // If-else statement
        if (mark < 50) {
            helloWorld.setTextColor(Color.RED);
            helloWorld.append("\nYou Lose !!!");
            return;
        }
        helloWorld.setTextColor(Color.GREEN);
        helloWorld.append("\nYou Win !!!");

    }
}
```

To launch the virtual device, go to `Device Manager` then `Create device`

![img_2.png](img_2.png)

After that, compile and start the application.

![img_3.png](img_3.png)

Voila, the first Android app has been created

![img.png](img.png)

![img_1.png](img_1.png)