 <img src="Screen.PNG" alt="Screen" width="50%" height="50%"> 

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