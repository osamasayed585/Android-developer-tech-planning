# Android developer tech planning
* [Core Android](#core-android)
* [Android Libraries](#android-libraries)
* [Android Architecture](#android-architecture)
* [Android Design Problem](#android-design-problem)
* [Android Unit Testing](#android-unit-testing)
* [Android Tools And Technologies](#android-tools-and-technologies)
* [Java and Kotlin](#java-and-kotlin)
* [Kotlin Coroutines](#kotlin-coroutines)
* [Kotlin Flow API](#kotlin-flow-api)
* [Jetpack Compose](#jetpack-compose)
* [Other Topics](#other-topics)
* [Data Structures and Algorithms](#data-structures-and-algorithms)

### Core Android

Android Interview Questions:

#### Base
* **What is Android? - [Learn from here](https://www.interviewbit.com/android-interview-questions/#what-is-android)
* **Tell all the Android application components.** <!-- - [Learn from here](https://developer.android.com/guide/components/fundamentals.html#Components)-->

* **What is `Context`? How is it used?** <!-- -  [Context In Android Application](https://amitshekhar.me/blog/context-in-android-application)-->

* **What is the project structure of an Android Application?** <!--- [Learn from here](https://developer.android.com/studio/projects)-->

* **What is `AndroidManifest.xml`?**

* **What is `Application` class?**
   <!-- - The Application class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any sublass of the Application class, is instantiated before any other class when the process for your application/package is created. -->

#### Activity and Fragment

* **Why is it recommended to use only the default constructor to create a `Fragment`?** <!-- - [Learn from here](https://www.youtube.com/watch?v=CitBt0FZFIc)-->

* **What is `Activity` and its lifecycle?**

* **What is the difference between onCreate() and onStart()**

* **When only onDestroy is called for an activity without onPause() and onStop()?** <!--- [Learn from here](https://www.youtube.com/watch?v=B2kY_ckZa-g)-->

* **Why do we need to call setContentView() in onCreate() of Activity class?** <!--- [Learn from here](https://www.youtube.com/watch?v=U1aHAt7XC5I)-->

* **What is onSavedInstanceState() and onRestoreInstanceState() in activity?**
    <!--- onSavedInstanceState() - This method is used to store data before pausing the activity.
    - onRestoreInstanceState() - This method is used to recover the saved state of an activity when the activity is recreated after destruction. So, the onRestoreInstanceState() receive the bundle that contains the instance state information.-->

* **What is `Fragment` and its lifecycle.**

* **What are "launchMode"?** <!--- [Learn from here](https://amitshekhar.me/blog/singletask-launchmode-in-android) and [singleTask launchMode in Android](https://youtu.be/WYkQEnm4jeI) -->

* **What is the difference between a `Fragment` and an `Activity`? Explain the relationship between the two.** <!--- [Learn from here](https://stackoverflow.com/questions/10478233/why-fragments-and-when-to-use-fragments-instead-of-activities) -->

* **When should you use a Fragment rather than an Activity?**
   <!-- - When you have some UI components to be used across various activities
    - When multiple view can be displayed side by side just like viewPager -->

* **What is the difference between FragmentPagerAdapter vs FragmentStatePagerAdapter?**
   <!-- - FragmentPagerAdapter: Each fragment visited by the user will be stored in the memory but the view will be destroyed. When the page is revisited, then the view will be created not the instance of the fragment.
    - FragmentStatePagerAdapter: Here, the fragment instance will be destroyed when it is not visible to the user, except the saved state of the fragment. -->

* **What is the difference between adding/replacing fragment in backstack?** <!--- [Learn from here](https://stackoverflow.com/questions/24466302/basic-difference-between-add-and-replace-method-of-fragment/24466345) -->

* **How would you communicate between two Fragments?**

* **What is retained `Fragment`?**
    <!--- By default, Fragments are destroyed and recreated along with their parent Activity’s when a configuration change occurs. Calling setRetainInstance(true) allows us to bypass this destroy-and-recreate cycle, signaling the system to retain the current instance of the fragment when the activity is recreated.-->

* **What is the purpose of `addToBackStack()` while commiting fragment transaction?**
    <!--- By calling addToBackStack(), the replace transaction is saved to the back stack so the user can reverse the transaction and bring back the previous fragment by pressing the Back button. <!--For more [Learn from here](https://stackoverflow.com/questions/22984950/what-is-the-meaning-of-addtobackstack-with-null-parameter)-->
#### Views and ViewGroups

* **What is `View` in Android?**

* **Difference between `View.GONE` and `View.INVISIBLE`?** <!-- [Learn from here](https://stackoverflow.com/questions/11556607/android-difference-between-invisible-and-gone)-->

* **Can you a create custom view? How?**

* **What are ViewGroups and how they are different from the Views?**
   <!-- - View: View objects are the basic building blocks of User Interface(UI) elements in Android. View is a simple rectangle box which responds to the user’s actions. Examples are EditText, Button, CheckBox etc. View refers to the android.view.View class, which is the base class of all UI classes.
    - ViewGroup: ViewGroup is the invisible container. It holds View and ViewGroup. For example, LinearLayout is the ViewGroup that contains Button(View), and other Layouts also. ViewGroup is the base class for Layouts.-->

* **What is a Canvas?**

* **What is a `SurfaceView`?** <!-- - [Learn from here](https://developer.android.com/reference/android/view/SurfaceView)-->

* **Relative Layout vs Linear Layout.**

* **Tell about Constraint Layout**

* **Do you know what is the view tree? How can you optimize its depth?** <!--- [Learn from here](https://developer.android.com/reference/android/view/ViewTreeObserver) -->

* **How does the Touch Control and Events work in Android?**

#### Displaying Lists of Content

* **What is the difference between `ListView` and `RecyclerView`?** <!--- [Learn from here](https://stackoverflow.com/questions/26728651/recyclerview-vs-listview)-->

* **How does RecyclerView work internally?**

* **What is the ViewHolder pattern? Why should we use it?** <!--- [Learn from here](https://stackoverflow.com/questions/21501316/what-is-the-benefit-of-viewholder-pattern-in-android) -->

* **RecyclerView Optimization - Scrolling Performance Improvement** <!--- [Learn from here](https://amitshekhar.me/blog/recyclerview-optimization)-->

* **Optimizing Nested RecyclerView** <!--- [Learn from here](https://amitshekhar.me/blog/setrecycledviewpool-for-optimizing-nested-recyclerview)-->

* **What is `SnapHelper`?** <!--- Learn from here: [SnapHelper](https://amitshekhar.me/blog/snaphelper) -->

#### Dialogs and Toasts

* **What is `Dialog` in Android?** <!--- [Learn from here](https://developer.android.com/guide/topics/ui/dialogs) -->

* **What is `Toast` in Android?** <!--- [Learn from here](https://developer.android.com/guide/topics/ui/notifiers/toasts)-->

* **What the difference between `Dialog` and `Dialog Fragment`?** <!--- [Learn from here](https://stackoverflow.com/questions/7977392/android-dialogfragment-vs-dialog) -->

#### Intents and Broadcasting

* **What is `Intent`?**

* **What is an Implicit `Intent`?**
        
* **What is an Explicit `Intent`?**

* **What is a `BroadcastReceiver`?** <!--- [Learn from here](https://developer.android.com/guide/components/broadcasts) -->

* **What is a `LocalBroadcastManager`?**

* **What is the function of an `IntentFilter`?** <!--- [Learn from here](https://developer.android.com/reference/android/content/IntentFilter) -->

* **What is a Sticky `Intent`?**
  <!--  - Sticky Intents allows communication between a function and a service. sendStickyBroadcast() performs a sendBroadcast(Intent) known as sticky, i.e. the Intent you are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver(BroadcastReceiver, IntentFilter). For example, if you take an intent for ACTION_BATTERY_CHANGED to get battery change events: When you call registerReceiver() for that action — even with a null BroadcastReceiver — you get the Intent that was last Broadcast for that action. Hence, you can use this to find the state of the battery without necessarily registering for all future state changes in the battery.-->

* **Describe how broadcasts and intents work to be able to pass messages around your app?** <!--- [Learn from here](https://stackoverflow.com/questions/7276537/using-a-broadcast-intent-broadcast-receiver-to-send-messages-from-a-service-to-a) -->

* **What is a `PendingIntent`?**
   <!-- - If you want someone to perform any Intent operation at future point of time on behalf of you, then we will use Pending Intent. -->

* **What are the different types of Broadcasts?** <!-- - [Learn from here](https://developer.android.com/guide/components/broadcasts) -->

#### Services

* **What is `Service`?** <!--  [Learn from here](https://developer.android.com/guide/components/services) -->

* **`Service` vs `IntentService`.**

* **What is a `JobScheduler`?** <!--- [Learn from here](https://developer.android.com/reference/android/app/job/JobScheduler) -->

#### Inter-process Communication

* **How can two distinct Android apps interact?** <!--- [Learn from here](https://developer.android.com/training/basics/intents) -->

<!--* **Is it possible to run an Android app in multiple processes? How?**  - [Learn from here](https://stackoverflow.com/questions/6567768/how-can-an-android-application-have-more-than-one-process)-->

* **What is AIDL? Enumerate the steps in creating a bounded service through AIDL.** <!--- [Learn from here](https://developer.android.com/guide/components/aidl)-->

* **What can you use for background processing in Android?** <!-- - [Learn from here](https://developer.android.com/guide/background) -->

* **What is a `ContentProvider` and what is it typically used for?** <!-- - [Learn from here](https://developer.android.com/guide/topics/providers/content-provider-basics) and [here](https://developer.android.com/guide/topics/providers/content-providers) -->

#### Long-running Operations

* **How to run parallel tasks in Java or Android, and get callback when all complete?** <!--- [Long-running tasks in parallel with Kotlin Flow](https://amitshekhar.me/blog/long-running-tasks-in-parallel-with-kotlin-flow) -->

* **Why should you avoid to run non-ui code on the main thread?** <!-- - [Learn from here](https://developer.android.com/training/multiple-threads/communicate-ui) -->

* **What is ANR? How can the ANR be prevented?** <!-- - [Learn from here](https://developer.android.com/topic/performance/vitals/anr.html) -->

* **What is an `AsyncTask`(Deprecated in API level 30) ?**

* **What are the problems in AsyncTask?**

* **When would you use java thread instead of an AsyncTask?** <!-- - [Learn from here](https://stackoverflow.com/questions/18480206/asynctask-vs-thread-in-android) -->

* **What is a `Loader`? (Deprecated)** <!-- - [Learn from here](https://developer.android.com/guide/components/loaders) -->

* **What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided?**
    <!--- An AsyncTask is not tied to the life cycle of the Activity that contains it. So, for example, if you start an AsyncTask inside an Activity and the user rotates the device, the Activity will be destroyed (and a new Activity instance will be created) but the AsyncTask will not die but instead goes on living until it completes.
    
    - Then, when the AsyncTask does complete, rather than updating the UI of the new Activity, it updates the former instance of the Activity (i.e., the one in which it was created but that is not displayed anymore!). This can lead to an Exception (of the type java.lang.IllegalArgumentException: View not attached to window manager if you use, for instance, findViewById to retrieve a view inside the Activity).
    
    - There’s also the potential for this to result in a memory leak since the AsyncTask maintains a reference to the Activity, which prevents the Activity from being garbage collected as long as the AsyncTask remains alive.

    - For these reasons, using AsyncTasks for long-running background tasks is generally a bad idea . Rather, for long-running background tasks, a different mechanism (such as a service) should be employed.
    
    - Note: AsyncTasks by default run on a single thread using a serial executor, meaning it has only 1 thread and each task runs one after the other. -->

* **Explain `Looper`, `Handler` and `HandlerThread`.**

* **Android Memory Leak and Garbage Collection**

#### Working With Multimedia Content

* **How do you handle bitmaps in Android as it takes too much memory?** <!-- - [Learn from here](https://developer.android.com/topic/performance/graphics/load-bitmap) and [here](https://developer.android.com/topic/performance/graphics/manage-memory) -->

* **What is the difference between a regular `Bitmap` and a nine-patch image?**
    <!--- In general, a Nine-patch image allows resizing that can be used as background or other image size requirements for the target device. The Nine-patch refers to the way you can resize the image: 4 corners that are unscaled, 4 edges that are scaled in 1 axis, and the middle one that can be scaled into both axes.

* **Tell about the `Bitmap` pool.** <!-- - [Learn from here](https://amitshekhar.me/blog/bitmap-pool) -->

* **How image compression is preformed?**

#### Data Saving

* **How to persist data in an Android app?**

* **What is ORM? How does it work?** 

* **How would you preserve `Activity` state during a screen rotation?** <!-- - [Learn from here](https://stackoverflow.com/questions/3915952/how-to-save-state-during-orientation-change-in-android-if-the-state-is-made-of-m)-->

* **What are different ways to store data in your Android app?**

* **Explain Scoped Storage in Android.**

* **How to encrypt data in Android?**

* **What is commit() and apply() in SharedPreferences?**
   <!-- - commit() returns a boolean value of success or failure immediately by writing data synchronously.
    - apply() is asynchronous and it won't return any boolean response. If you have an apply() outstanding and you are performing commit(), then the commit() will be blocked until the apply() is not completed.-->

#### Look and Feel

* **What is a `Spannable`?**

* **What is a `SpannableString`?**
   <!--- A SpannableString has immutable text, but its span information is mutable. Use a SpannableString when your text doesn't need to be changed but the styling does. Spans are ranges over the text that include styling information like color, heighliting, italics, links, etc -->

* **What are the best practices for using text in Android?**

* **How to implement Dark mode in any application?**

* **How to generate dynamic colors based in image?**

* **Explain about Density Independence Pixel**

#### Memory Optimizations

* **What is the `onTrimMemory()` method?** <!-- - [Learn from here](https://developer.android.com/topic/performance/memory) -->

* **How does the OutOfMemory happens?**

* **How do you find memory leaks in Android applications?**

#### Battery Life Optimizations

* **How to reduce battery usage in an android application?**

* **What is Doze? What about App Standby?** <!-- - [Learn from here](https://developer.android.com/training/monitoring-device-state/doze-standby) -->

* **What is `overdraw`?** <!--- [Learn from here](https://developer.android.com/topic/performance/rendering/overdraw.html) -->

#### Supporting Different Screen Sizes

* **How do you support different types of resolutions?** <!--- [Learn from here](https://developer.android.com/training/multiscreen/screensizes) -->

#### Permissions

* **What are the different protection levels in permission?**

#### Native Programming

* **What is the NDK and why is it useful?** <!--- Learn from here: [Android NDK and RenderScript](https://amitshekhar.me/blog/ndk-and-renderscript) -->

* **What is renderscript?** - Learn from here: <!-- [Android NDK and RenderScript](https://amitshekhar.me/blog/ndk-and-renderscript) -->

#### Android System Internal

* **What is Android Runtime?** <!--- [Android Runtime](https://amitshekhar.me/blog/dalvik-art-jit-aot) -->

* **Dalvik, ART, JIT, and AOT in Android** <!--- [Dalvik, ART, JIT, and AOT](https://amitshekhar.me/blog/dalvik-art-jit-aot) -->

* **What are the differences between Dalvik and ART?** <!--- [Difference between Dalvik and ART](https://amitshekhar.me/blog/dalvik-art-jit-aot)-->

* **What is DEX?** <!--- [Learn from here](https://developer.android.com/reference/dalvik/system/DexFile) -->

* **Can you manually call the Garbage collector?** <!--- [Is it possible to force Garbage Collection in Android?](https://www.youtube.com/watch?v=fPEjpFKo1-Q) -->

#### Android Jetpack

* **What is Android Jetpack and why to use this?**

* **What is a ViewModel and how is it useful?** Learn:<!--  [What is a ViewModel and how is it useful?](https://youtu.be/ORtieK5f_zg) -->

* **What are Android Architecture Components?**

* **What is LiveData in Android?**

* **How LiveData is different from ObservableField?**

* **What is the difference between setValue and postValue in LiveData?**

* **How to share ViewModel between Fragments in Android?**

* **Explain Work Manager in Android.**

* **Use-cases of WorkManager in Android.**

* **How ViewModel work internally?**

#### Others

* **Why Bundle class is used for data passing and why cannot we use simple Map data structure?** <!--- [Learn from here](https://developer.android.com/guide/components/activities/parcelables-and-bundles) -->

* **How do you troubleshoot a crashing application?** <!--- [Learn from here](https://developer.android.com/topic/performance/vitals/crash)-->

* **Explain Android notification system?** - How does the Android notification system work? <!--(https://youtu.be/810IFG2sWlc)-->

* **What is the difference between Serializable and Parcelable? Which is the best approach in Android?**

* **What is AAPT?** <!-- - [Learn from here](https://developer.android.com/studio/command-line/aapt2) -->

* **What is the best way to update the screen periodically?** <!--- [Learn from here](https://stackoverflow.com/questions/5452394/best-way-to-perform-an-action-periodically-while-an-app-is-running-handler)-->

* **FlatBuffers vs JSON.**

* **`HashMap`, `ArrayMap` and `SparseArray`**

* **What are Annotations?**

* **How to create custom Annotation?**

* **How to handle multi-touch in android?**

* **What is the support library? Why was it introduced?**

* **What is Android Data Binding?**

* **How to check if Software keyboard is visible or not?**

* **How to take screenshot in Android programmatically?**

### Android Libraries

Android Interview Questions:

* **Explain OkHttp Interceptor** <!--- [Learn from here](https://amitshekhar.me/blog/okhttp-interceptor)-->

* **OkHttp - HTTP Caching** <!--- [Learn from here](https://amitshekhar.me/blog/caching-with-okhttp-interceptor-and-retrofit)-->

* **Tell me something about RxJava.**

* **How will you handle error in RxJava?**

* **FlatMap Vs Map Operator** <!--- [Learn from here](https://amitshekhar.me/blog/rxjava-map-vs-flatmap)-->
    
* **When to use `Create` operator and when to use `fromCallable` operator of RxJava?** <!--- Learn from here: [RxJava Create and fromCallable Operator](https://amitshekhar.me/blog/rxjava-create-and-fromcallable-operator)-->
    
* **When to use `defer` operator of RxJava?** - Learn from here:<!-- [RxJava Defer Operator](https://amitshekhar.me/blog/rxjava-defer-operator)-->
    
* **How are Timer, Delay, and Interval operators used in RxJava?** <!--- [Learn from here](https://amitshekhar.me/blog/rxjava-interval-operator)-->

* **How to make two network calls in parallel using RxJava?** - <!--[RxJava Zip Operator](https://amitshekhar.me/blog/rxjava-zip-operator)-->
    
* **Tell the difference between Concat and Merge.** <!--- [Learn from here](https://amitshekhar.me/blog/rxjava-concat-operator) and [here](https://amitshekhar.me/blog/rxjava-merge-operator) -->

* **Explain Subject in RxJava?** <!--- [Learn from here](https://amitshekhar.me/blog/rxjava-subject-publish-replay-behavior-async)-->

* **What are the types of Observables in RxJava?** <!--- Learn from here: [Types Of Observables In RxJava](https://amitshekhar.me/blog/types-of-observables-in-rxjava)-->

* **How to implement search feature using RxJava in your application?**<!-- - Learn from here: [Instant Search Using RxJava Operators](https://amitshekhar.me/blog/instant-search-using-rxjava-operators)-->

* **Pagination In RecyclerView Using RxJava Operators** <!--- [Learn from here](https://amitshekhar.me/blog/pagination-in-recyclerview-using-rxjava-operators)-->

* **How The Android Image Loading Library Glide and Fresco Works?**<!--- [Learn from here](https://amitshekhar.me/blog/android-image-loading-library-optimize-memory-usage), [here](https://amitshekhar.me/blog/android-image-loading-library-use-bitmap-pool-for-responsive-ui) and [here](https://amitshekhar.me/blog/android-image-loading-library-solve-the-slow-loading-issue)-->

* **Difference between Schedulers.io() and Schedulers.computation() in RxJava.**

* **Why do we use the Dependency Injection Framework like Dagger in Android?**

* **How does the Dagger work?**

* **What is Component in Dagger?**

* **What is Module in Dagger?**

* **How does the custom scope work in Dagger?**

* **When to call dispose and clear on CompositeDisposable in RxJava?**<!-- - [Learn from here](https://amitshekhar.me/blog/dispose-vs-clear-compositedisposable-rxjava)-->

* **What is Multipart Request in Networking?**

* **What is Flow in Kotlin?** <!--- [Learn from here](https://amitshekhar.me/blog/flow-api-in-kotlin) -->

### Android Architecture

Android Interview Questions:

* **Describe the architecture of your last app.**

* **Describe MVP.**

* **Describe MVVM.** <!--- [MVVM Architecture](https://amitshekhar.me/blog/mvvm-architecture-android) -->

* **MVC vs MVP vs MVVM architecture.**

* **What is presenter?**

* **What is model?**

* **Describe MVC.**

* **Describe MVI**

* **Describe the repository pattern**

* **What is controller?**

* **Tell something about clean code**

### Android Design Problem

Android Interview Questions:

* **Design Uber App.** <!--- [Learn from here](https://github.com/amitshekhariitbhu/ridesharing-uber-lyft-app)-->

* **Design Facebook App.**

* **Design Facebook Near-By Friends App.**

* **Design WhatsApp.**

* **Design SnapChat.**

* **Design problems based on location based app.**

* **How to build offline-first app? Explain the architecture.**

* **Design LRU Cache.**

* **Design File Downloader** <!--- [Learn from here](https://github.com/amitshekhariitbhu/PRDownloader)-->

* **Design an Image Loading Library** <!--- [Learn from here](https://amitshekhar.me/blog/android-image-loading-library-optimize-memory-usage), [here](https://amitshekhar.me/blog/android-image-loading-library-use-bitmap-pool-for-responsive-ui) and [here](https://amitshekhar.me/blog/android-image-loading-library-solve-the-slow-loading-issue)-->

* **HTTP Request vs HTTP Long-Polling vs WebSockets** <!--- [Learn from blog](https://amitshekhar.me/blog/http-request-long-polling-websocket-sse) and [Video - HTTP Request vs HTTP Long-Polling vs WebSocket vs Server-Sent Events](https://www.youtube.com/watch?v=8ksWRX4xV-s)-->

* **How do Voice And Video Call Work?** <!--- [Learn from here](https://amitshekhar.me/blog/voice-and-video-call)-->

### Android Unit Testing

Android Interview Questions:

* **What is Espresso?** <!--- [Learn from here](https://developer.android.com/training/testing/ui-testing/espresso-testing.html) -->

* **What is Robolectric?** <!--- [Learn from here](http://robolectric.org/) -->

* **What are the disadvantages of using Robolectric?** <!--- [Learn from here](https://stackoverflow.com/questions/18271474/robolectric-vs-android-test-framework) -->

* **What is UI-Automator?** <!--- [Learn from here](https://developer.android.com/training/testing/ui-testing/uiautomator-testing.html) -->

* **Explain unit test.** <!--- [Learn from here](https://developer.android.com/training/testing/unit-testing/local-unit-tests) -->

* **Explain instrumented test.** <!--- [Learn from here](https://developer.android.com/training/testing/unit-testing/instrumented-unit-tests) -->

* **Have you done unit testing or automatic testing?**

* **Why Mockito is used?** <!--- [Learn from here](http://site.mockito.org/) -->

* **Describe JUnit test.** <!--- [Learn from here](https://en.wikipedia.org/wiki/JUnit) -->

* **Describe code coverage.**

### Android Tools And Technologies

Android Interview Questions:

* **What is ADB?** <!--- [Learn from here](https://developer.android.com/studio/command-line/adb) -->

* **What is DDMS and what can you do with it?** <!--- [Learn from here](https://developer.android.com/studio/profile/monitor)-->

* **What is the StrictMode?** <!--- Learn from here: [StrictMode](https://amitshekhar.me/blog/strictmode-in-android-development) -->

* **What is Lint? What is it used for?**

* **Git.**

* **Android Development Useful Tools.**

* **Firebase.** <!-- [Learn from here](https://firebase.google.com/) -->

* **How to measure method execution time in Android?**

* **Can you access your database of SQLite Database for debugging?** <!--- [Learn from here](https://github.com/amitshekhariitbhu/Android-Debug-Database)-->

* **What are things that we need to take care while using Proguard?**

* **What is Multidex in Android?**

* **How to use Android Studio Memory Profiler?**

* **How to use Firebase realtime database in your app?**

* **What is Gradle?**

* **APK Size Reduction.**

* **How can you speed up the Gradle build?**

* **About gradle build system.**

* **About multiple apk for android application.**

* **What is proguard used for?**

* **What is obfuscation? What is it used for? What about minification?**

* **How to change some parameters in an app without app update?**

### Java and Kotlin

Android Interview Questions:

#### OOP

* **Explain OOP Concepts.**
    - Object-Oriented Programming is a methodology of designing a program using classes, objects, 
    [inheritance](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)),
    [polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)),
    [abstraction](https://en.wikipedia.org/wiki/Abstraction_(software_engineering)), and
    [encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)).
    
* **What is the difference between a constructor and a method?**
    - The name of the constructor is same as that of the class name, whereas the name of the method can be anything.
    - There is no return type of a constructor.
    - When you make an object of a class, then the constructor of that class will be called automatically. 
      But for methods, we need to call it explicitely.
    - Constructors can't be inherited but you can call the constructor of the parent class by calling `super()`.
    - Constructor and a method they both run a block of code but the difference is in calling them.
    - We can call method directly using their name.
    - Constructor Syntax -
        ```java
        public class SomeClassName{
            SomeClassName(parameter_list){ 
                ...
            } 
            ...
        }
        ```
    - Note:
        In the above syntax, the name of the constructor is the same as that of class
        and it has no return type.
        
    - Method Syntax 
        ```java
        public class SomeClassName{
            public void someMethodName(parameter_list){
                ...
            }
            // call method
            someMethodName(parameter_list)
        }
        ```
