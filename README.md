# InstaDotView

InstaDotView is a customizable dot indicator for Android that can be used to display the current page in a view pager.

## Usage

### Step 1: Add JitPack Repository

Add JitPack to your root `build.gradle` file:

```groovy
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```

### Step 2: Add the Dependency

Add the following dependency in your app's build.gradle:
```gradle

dependencies {
    implementation 'com.github.AnurupJaiswal:InstaDotIndicatorLibrary:1.0.0'
}
```
### Step 3: Layout

 In your XML layout file, add the InstaDotView with the attributes of your choice:
 
```xml
<com.anurupjaiswal.instadot.InstaDotView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        app:dot_activeColor="@color/colorAccent"
        app:dot_activeSize="10dp"
        app:dot_inactiveColor="@color/colorPrimaryDark"
        app:dot_inactiveSize="8dp"
        app:dot_margin="10dp"
        app:dot_mediumSize="6dp"
        app:dot_smallSize="4dp" />
```
### Step 4: Set Number of Pages
[REQUIRED] 
Set the number of pages using:
```Kotlin
instaDotViewInstance.onPageChange(pageNo)
```
### Step 5: Update Dot on Page Change
[REQUIRED] update dot on page change:
```kotlin
instaDotViewInstance.onPageChange(pageNo)
```
[OPTIONAL] Set Number of Visible Items
You can set the number of visible items (must be greater than the default value of 6):
```Kotlin
instaDotViewInstance.setVisibleDotCounts(pages)
```
### Attributes for customization

## If none of the following attributes are set, all default values will be used:

```
   <attr name="dot_activeColor" format="color" />
   <attr name="dot_inactiveColor" format="color" />
   <attr name="dot_activeSize" format="dimension" />
   <attr name="dot_inactiveSize" format="dimension" />
   <attr name="dot_mediumSize" format="dimension" />
   <attr name="dot_smallSize" format="dimension" />
   <attr name="dot_margin" format="dimension" />
   <attr name="dots_visible" format="integer" />
```

![instadot_demo](https://github.com/user-attachments/assets/2ef1b383-f44b-4aa2-9220-41d4e2d310ea)


