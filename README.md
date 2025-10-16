# HackerSpacesQuiz


```
https://github.com/AKNoryx28/Android-ImGui-GLSurfaceView
https://github.com/Ciremun/imgui-android
```


📍 From your project folder:

```
/home/when/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android


```



⚙️ Build Debug APK


```
./gradlew assemble
```



when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android$ ./gradlew assembleDebug

> Task :app:checkDebugAarMetadata
Caught exception: Already watching path: /home/when/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android

[Incubating] Problems report is available at: file:///home/when/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/build/reports/problems/problems-report.html

Deprecated Gradle features were used in this build, making it incompatible with Gradle 10.0.

You can use '--warning-mode all' to show the individual deprecation warnings and determine if they come from your own scripts or plugins.

For more on this, please refer to https://docs.gradle.org/9.0-milestone-1/userguide/command_line_interface.html#sec:command_line_warnings in the Gradle documentation.

BUILD SUCCESSFUL in 38s
42 actionable tasks: 42 executed
when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android$ 




### (Optional) Sign release APK


```

ngl3/android/app/build/outputs/apk/release$ pwd
/home/when/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release
when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ 

```




Make it using this command 👇


💬 It will ask:

Keystore password → choose any strong one

Your name, org, city, country → can be anything

Key password → can be same as keystore password



```

keytool -genkey -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-key-alias


```

hackerspace@2025





ngl3/android/app/build/outputs/apk/release$ keytool -genkey -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-key-alias
'Enter keystore password:  
Re-enter new password: 
Enter the distinguished name. Provide a single dot (.) to leave a sub-component empty or press ENTER to use the default value in braces.
What is your first and last name?
  [Unknown]:  tpj_root
What is the name of your organizational unit?
  [Unknown]:  
What is the name of your organization?
  [Unknown]:  hackerspaces
What is the name of your City or Locality?
  [Unknown]:  TPJ
What is the name of your State or Province?
  [Unknown]:  TN
What is the two-letter country code for this unit?
  [Unknown]:  IN
Is CN=tpj_root, OU=Unknown, O=hackerspaces, L=TPJ, ST=TN, C=IN correct?
  [no]:  yes

Generating 2,048 bit RSA key pair and self-signed certificate (SHA384withRSA) with a validity of 10,000 days
	for: CN=tpj_root, OU=Unknown, O=hackerspaces, L=TPJ, ST=TN, C=IN
[Storing my-release-key.jks]
when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ 






After done, you’ll get
my-release-key.jks






apksigner is part of the Android SDK (Build Tools) — it comes with Android Studio.



when@master:~/Downloads/SIFTWARES/android-studio-2025.1.3.7-linux/android-studio$ cd ~/Android/Sdk/build-tools/
when@master:~/Android/Sdk/build-tools$ ls
34.0.0  35.0.0  35.0.1  36.1.0
when@master:~/Android/Sdk/build-tools$ 



~/Android/Sdk/build-tools/<version>/apksigner



~/Android/Sdk/build-tools/36.1.0/apksigner




~/Android/Sdk/build-tools/34.0.0/apksigner sign --ks my-release-key.jks --out app-release-signed.apk app-release-unsigned.apk






when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ m5
a6193e2acf43fe4323c97eaf1e0f5cf7  app-release-unsigned.apk
26b1b0c04748c5544cb4fa489f50cd82  my-release-key.jks
cdef7bcfc974ef7a95524e1a10c35b8c  output-metadata.json



when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ ~/Android/Sdk/build-tools/34.0.0/apksigner sign --ks my-release-key.jks --out app-release-signed.apk app-release-unsigned.apk
when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ m5
a0b809d3d76d001bbba7bfda39c50393  app-release-signed.apk
3c3006223b74b5e2bed36121f9fa6af5  app-release-signed.apk.idsig
a6193e2acf43fe4323c97eaf1e0f5cf7  app-release-unsigned.apk
26b1b0c04748c5544cb4fa489f50cd82  my-release-key.jks
cdef7bcfc974ef7a95524e1a10c35b8c  output-metadata.json
when@master:~/Desktop/MY_GIT/HackerSpacesQuiz/imgui/examples/example_android_opengl3/android/app/build/outputs/apk/release$ 



