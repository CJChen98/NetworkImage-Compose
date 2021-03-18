# NetworkImage-Compose

A  Jetpack Compose library that provides Compose support for Glide.

## Usage

1. Add the dependency

```groovy
 dependencies {
    implementation 'cn.chitanda.compose:network-image:0.0.4'
 }
```

2. Provide a Glide `RequestManager` instance to your root Compose tree:

```kotlin
 setContent { 
     ProvideGlideLoader {
    	Home()
 	}
 }
```

```kotlin
NetworkImage(
    url: String,/*image url */
    modifier: Modifier = Modifier,
    contentDescription: String? = null,
    onLoading: {/* the widget to be displayed while the image is being downloaded*/ },
    onFailure: {/* the widget to be displayed if an error occurs*/},
) 
```

