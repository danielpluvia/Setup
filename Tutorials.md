# Tutorials

## iOS

### iOS Animation

* [Getting Started](https://www.raywenderlich.com/363-ios-animation-tutorial-getting-started)

    Explains the basic ideas of Animation (**Very usefull**)

* [UIViewController Transitions](https://www.raywenderlich.com/322-custom-uiviewcontroller-transitions-getting-started)
  * [How To Make A UIViewController Transition Animation Like in the Ping App](https://www.raywenderlich.com/261-how-to-make-a-uiviewcontroller-transition-animation-like-in-the-ping-app)

* Transform

  * [Using Perspective Transforms](https://guides.codepath.com/ios/Using-Perspective-Transforms)
  * [INTRODUCTION TO 3D DRAWING IN CORE ANIMATION (PART 1)](http://www.thinkandbuild.it/introduction-to-3d-drawing-in-core-animation-part-1/)
  * [3D变换](https://zsisme.gitbooks.io/ios-/content/chapter5/3d-transform.html)
    * ❕[iOS Core Animation: Advanced Techniques中文译本](https://zsisme.gitbooks.io/ios-/content/index.html)

* [Why We Don’t Use Interface Builder and Storyboards at Instabug](https://instabug.com/blog/why-we-dont-use-interface-builder-and-storyboards-at-instabug/)

## CocoaPod

### [Using Pod Lib Create](https://medium.com/@satishios25/creating-and-publishing-a-custom-pod-to-cocoapods-library-b314c3c7b4f0)

* Go go [Github](github.com) website and create a new **empty** respository, which is called `MyLibrary`. This repository MUST NOT contain any files.
* `pod lib create MyLibrary` (The name should match the GitHub repo).
* Go to the folder `Example` and open `*.xcworkspace`.
* Sign the project and modify `Podfile` (remove the version number of Quick and Nimble).
* Run `pod update` again to fix the `Quick: No such module` problem.
* **Go back to the root directory of the project**. Push our new pod library to the GitHub repository we created prior.

  ~~~batch
    git init
    git add -A
    git commit -m "Initial commit with cocoapod lib template"
    git remote add origin https://github.com/xxxxxxxx/MyLibrary.git ~ "Replace with your remote URL"
    git push -u origin master
  ~~~

* `Command + k` and `Command + Shift + k` to clean the project.
* Then developing the framework (make sure the class or method is `public`, so that it can be accessed by the project).
* To use the Framework, you need to import `MyLibrary` in the file where you want to use `MyLibrary`.
* Go to folder `Podspec Metadata` to modify file `DPSwiftExtension.podspec`.
* Make sure you have provided content for summary , description (longer than summary) and check you swift version (add `s.swift_version = '4.2'` to the file).
* In Terminal: go back to the root directory of the project.
* Run

  ```batch
  pod lib lint MyLibrary.podspec
  ```

* Push all your code to GitHub repo.
* The next thing we need to do is create a tag release in this repo.
* Create a tag release in this repo. It should exactly match the podspec version we have.

  ```batch
  git tag '0.0.1'
  git push --tags
  ```

* Register our mail id via trunk. (Optional)

  ```batch
  pod trunk register 'Your email ID'
  ```

* Submitting Open Source Code. Push our pod up to trunk.
  
  ```batch
  pod trunk push MyLibrary.podspec
  ```

#### References

* https://medium.com/@satishios25/creating-and-publishing-a-custom-pod-to-cocoapods-library-b314c3c7b4f0