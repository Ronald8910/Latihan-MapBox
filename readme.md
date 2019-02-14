1. install mapbox pacage
    $ npm i @mapbox/react-native-mapbox-gl

2. go to yourproject/android/build.gradle java
Tambahkan:
            maven { url "https://jitpack.io" }
            maven { url "https://maven.google.com" }

        }
    }
}

3. go to your project/android/app/build.gradle

tambahkan di dependencies:
compile project(':mapbox-react-native-mapbox-gl')
}

4. go to your project/android/setting.gradle
tambahkan di baris paling bawah:

include ':mapbox-react-native-mapbox-gl'
project(':mapbox-react-native-mapbox-gl').projectDir = new File(rootProject.projectDir, '../node_modules/@mapbox/react-native-mapbox-gl/android/rctmgl')

5. go to yourProject/android/app/src/main/java/com/yourProject/MainApplication.java

insert after import com.facebook.soloader.SoLoader:
tambahkan:

import com.mapbox.rctmgl.RCTMGLPackage;
insert inside getPackages() after new MainReactPackage(),

new RCTMGLPackage()

6. sign up To MapBox [www.mapbox.com]

Default Token MapBox
pk.eyJ1Ijoicm9uYWxkMTA4OSIsImEiOiJjanM0MmR0cXQwMGxoNGFvYjByZXloY2h2In0.NID8d5FT6aDiYz3nq44SOQ
(./1.png)
# Latihan-MapBox
