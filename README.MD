 
 <h2> build.gradle.kts (Module :app) </h2>

 ```gradle

     buildFeatures {
        viewBinding = true
    }

    buildTypes {
        create("customDebugType") {
            isDebuggable = true
        }
    }

 ```

<br/>
 <img src="Screen.PNG" alt="Screen" width="50%" height="50%"> 

<br/>

 <h2> MainActivity.kt </h2>

  ```kotlin


package com.example.androidlesson1

import android.graphics.Color
import android.os.Bundle
import androidx.activity.enableEdgeToEdge
import androidx.appcompat.app.AppCompatActivity
import androidx.core.view.ViewCompat
import androidx.core.view.WindowInsetsCompat
import com.example.androidlesson1.databinding.ActivityMainBinding

class MainActivity : AppCompatActivity() {

    lateinit var binding: ActivityMainBinding

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()

        binding = ActivityMainBinding.inflate(layoutInflater)
        setContentView(binding.root)

        binding.button.setOnClickListener {
            val name = binding.editText1.text.toString().trim()
            val password = binding.editText2.text.toString().trim()
            val email = binding.editText3.text.toString().trim()

            if (name != "Name" && password != "Password" && email != "Email") {
                binding.textView.text = "$name -- $password -- $email"
            } else {
                binding.textView.setTextColor(Color.parseColor("#FF0000"))
                binding.textView.text = "Do not leave the textbox empty"
            }

        }
    }
}



 ```
