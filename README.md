# mathjs-android

[![Build Status](https://travis-ci.org/niltonvasques/mathjs-android.svg?branch=travis)](https://travis-ci.org/niltonvasques/mathjs-android)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-MathJS%20Android-green.svg?style=flat)](http://android-arsenal.com/details/1/4675)

An android wrapper library to mathjs.org javascript library

## Installation

#### Gradle
Mathjs is available on jitpack.

Add jitpack to your root build.gradle:

```gradle
	allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
```

Add the library to app build.gradle

```gradle
    compile 'com.github.niltonvasques:mathjs-android:v0.1.2'
```

### Usage
```java
    MathJS math = new MathJS(getApplicationContext());
    math.eval("2 * 5 ^ 2", new MathJS.MathJSResult() {
        @Override
        public void onEvaluated(String value) {
            System.out.println("MathJS.onEvaluated "+value);
        }
    });
    math.eval("2 * 5 ^ 2 + 33", new MathJS.MathJSResult() {
        @Override
        public void onEvaluated(String value) {
            System.out.println("MathJS.onEvaluated "+value);
        }
    });
    
    math.destroy(); //Call after the library been used
```
