
<p align="center">
  <img width="560" height="120" src="https://camo.githubusercontent.com/ed508e9c66d718f76333215a139af24f8bb8fa8d/68747470733a2f2f6d75736573636f72652e6f72672f73697465732f6d75736573636f72652e6f72672f66696c65732f4361707475726525323064253237652543432538316372616e253230323031362d30332d303125323030392e34382e31315f302e706e67">
</p>

## Google Summer of Code 2018 Work Report 

| Field | Details |
| --- | --- |
| **Student** | **Siddharth Sharma** |
| **Github** | [@siddharth2010](http://github.com/siddharth2010)  |
| **Organisation**  | [Kiwix](https://www.kiwix.org/)  |
| **Project** | [Kiwix Android Testing](https://summerofcode.withgoogle.com/projects/#5441752727552000) |  

## Organisation
![Kiwix](http://www.kiwix.org/wp-content/uploads/2016/06/KiwixLogo_horizontal_contours.png)

**[Kiwix](https://github.com/kiwix)** enables you to have the whole Wikipedia at hand wherever you go! It is an offline solution that allows you to access educational content like Wikipedia, the Wiktionary, TED talks and many others on any computer or smartphone - without the need for a live internet connection.

## Project Description

### Improve the Kiwix Android apps CI setup and increase our code coverage
This required improving the app architecture and making the package structure more robust, followed by creation of local unit tests, as well as instrumentation tests for the app, and refactoring the previous tests, tailoring them according to the app architecture.


#### Work Done
I started off by understanding how to libraries like [Dagger2](https://google.github.io/dagger/users-guide) work. I then tried to get some insights into the [architecture](https://github.com/googlesamples/android-architecture) of an android app (especially the MVP architecture).
This was followed up by learning the principles of [RxJava](http://reactivex.io/RxJava/javadoc/), and tried to implement it using the [MVP RxJava](https://github.com/googlesamples/android-architecture/tree/todo-mvp-rxjava/) architecture in a test app. I then tried to understand the working of [Travis](https://docs.travis-ci.com/) and [Bitbar](http://docs.bitbar.com/), and also the working of testing libraries like JUnit, and Mockito, and Espresso by making a test apps to get a hang on how testing actually happens.

I started off with my work on the app by proposing a more robust package structure. I tried to use RxJava and Lambda Expressions, to change some of the view callbacks like click events. However, this idea was dropped after a few weeks, as a lot of changes were simultaneously being made to the UI/UX of the app (requiring most of the screens to be build from scratch).

After that, I started off with testing, making Unit tests for most of the Helper classes, and some other POJOs in use throughout the app. This was followed up by testing the internal database, using instrumentation tests. And then in the end, I did some UI tests, testing isolated views, as well as cases where interactivity data was being passed.

## Personal Experience
This was my first time working on a complex android project and I had a great time doing it. The last few months really changed my perspective about software development in general. Over the course of these three months I learnt how to write professional code, and understood the importance of documentation and coding conventions. This was also the first time I was working with different libraries (like squidb, powermockito), and I finally understood how to read the documentation and implement the library myself, instead of searching the web for a walkthrough. This was my first experience of working in a professional setting, and I had some really helpful friends and mentors who made the experience a fun ride, helping me whenever I got stuck (which happened a lot of times).

## Link to Commits
Heres a [link](https://github.com/kiwix/kiwix-android/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Asiddharth2010+created%3A2018-04-23..2018-08-14+) to the work I did.

## Future Work
Even though quite a lot of my work is done, there are many more improvements that still can be made in testing. I plan to write some more UI tests, and also improve some of the existing tests. I also plan on testing the database in a different way, starting from scratch, using the JVM tests instead of the standard integration tests that we are doing as of now. I do plan to work on these things in the coming months.