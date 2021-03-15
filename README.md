# NetworkImage-Compose [![](https://jitpack.io/v/CJChen98/NetworkImage-Compose.svg)](https://jitpack.io/#CJChen98/NetworkImage-Compose)

A  Jetpack Compose library that provides Compose support for Glide.

## Setup

1. Add it in your root `build.gradle` at the end of repositories:

```groovy
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

2. Add the dependency

```groovy
dependencies {
	        implementation 'com.github.CJChen98:NetworkImage-Compose:0.0.3'
	}
```

3. Provide a Glide `RequestManager` instance to your root Compose tree:

```kotlin
 setContent { 
     ProvideGlideLoader {
    	SampleScreen()
 	}
 }
```



## Usage

```kotlin
NetworkImage(
    url: String,/*image url */
    modifier: Modifier = Modifier,
    contentDescription: String? = null,
    onLoading: {/* the widget to be displayed while the image is being downloaded*/ },
    onFailure: {/* the widget to be displayed if an error occurs*/},
) 
```

