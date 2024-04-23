 <img src="Screen.PNG" alt="Screen" width="50%" height="50%"> 

 ```kotlin

     buildFeatures {
        viewBinding = true
    }

    buildTypes {
        create("customDebugType") {
            isDebuggable = true
        }
    }

 ```