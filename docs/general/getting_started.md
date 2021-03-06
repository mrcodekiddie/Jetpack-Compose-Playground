# Project Setup

!!! info
        Note: Jetpack Compose is currently in Developer Preview. The API surface is not yet finalized, and changes are planned and expected. See the Compose Compiler and Runtime release notes and the Compose UI release notes for the latest updates.

## Android Studio
To use Jetpack Compose you need to use at least a [version >= Android Studio Arctic Fox Canary 7](https://developer.android.com/studio/preview)

## Gradle Dependencies

Add this inside in the **android{}** block your build.gradle
```groovy
android{
//YOUR OTHER CODE

    kotlinOptions {
        jvmTarget = '1.8'
        useIR = true
    }
    buildFeatures {
        compose true
    }
    composeOptions {
        kotlinCompilerExtensionVersion "1.0.0-alpha12"
        kotlinCompilerVersion '1.4.30'
    }

}
```

Below are some Compose dependencies that are online available, can find the others [here](https://maven.google.com/web/index.html?q=compose#androidx.compose.ui)

```groovy

dependencies {
    def compose_version = "1.0.0-alpha12"

    implementation "androidx.compose.animation:animation-core:$compose_version"
    implementation "androidx.compose.animation:animation:$compose_version"
    implementation("androidx.compose.ui:ui:$compose_version")
    implementation "androidx.compose.foundation:foundation:$compose_version"
    implementation "androidx.compose.ui:ui-geometry:$compose_version"
    implementation "androidx.compose.ui:ui-graphics:$compose_version"
    implementation "androidx.compose.foundation:foundation-layout:$compose_version"
    implementation "androidx.compose.runtime:runtime-livedata:$compose_version"
    implementation "androidx.compose.material:material:$compose_version"
    implementation "androidx.compose.material:material-icons-core:$compose_version"
    implementation "androidx.compose.material:material-icons-extended:$compose_version"
    implementation "androidx.compose.runtime:runtime-rxjava2:$compose_version"
    implementation("androidx.compose.ui:ui-text:$compose_version")
    implementation("androidx.compose.ui:ui-util:$compose_version")
    implementation ("androidx.compose.ui:ui-viewbinding:$compose_version")
    implementation "androidx.compose.ui:ui-tooling:$compose_version"

    //Compose Constraintlayout
    implementation 'androidx.constraintlayout:constraintlayout-compose:1.0.0-alpha02'


}

```
