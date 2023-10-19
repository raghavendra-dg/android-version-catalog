# Version Catalog for android apps
![Version](https://img.shields.io/maven-central/v/io.github.raghavendra-dg/version-catalog-android?style=flat-square)

## Usage

You need to add version catalog in `settings.gradle.kts` from remote repository:

```kotlin
dependencyResolutionManagement {
    repositories {
        mavenCentral()
    }

    versionCatalogs {
        create("libs") {
            from("io.github.raghavendra-dg:version-catalog-android:1.0.0")
        }
    }
}
```
After the sync gradle create accessors from dependencies like:

```kotlin
plugins {
    alias(libs.plugins.android.kotlin)
    alias(libs.plugins.android.application)
}

dependency{
    implementation(libs.ui)
    implementation(libs.material3)
}
```