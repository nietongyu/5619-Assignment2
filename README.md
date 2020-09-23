# Assignment 2: Creating Virtual Environments

**Due: Monday, September 27, 10:00pm CDT**

The purpose of this assignment is for you to gain experience creating virtual environments in Babylon.  A template project has been provided with an empty scene.  Your goal is to create your own virtual environment using free 3D art assets found on the web, with the following requirements:

- The environment should be an outdoor scene.
- The models should include materials with textures.
- You should not use any of the assets that were already provided in previous lectures or assignments.

You are free to use any legal sources for third party assets, including downloading models from websites such as [Clara.io](https://clara.io/).  Alternatively, you can also locate and export assets from the [Unity Asset Store](https://assetstore.unity.com/), as shown in [Lecture 2](https://github.com/CSCI-5619-Fall-2020/Lecture-2).

Creativity is encouraged!

## Submission Information

You should fill out this information before submitting your assignment.  Make sure to document the name and source of any third party assets such as 3D models, textures, or any other content used that was not solely written by you.  Include sufficient detail for the instructor or TA to easily find them, such as asset store or download links.

Name: 

UMN Email:

Build URL:

Third Party Assets:

## Rubric

Graded out of 10 points.  Each of the parts to be added are presented in lecture or covered in the [Babylon 101](https://doc.babylonjs.com/babylon101/) and [Babylon How To](https://doc.babylonjs.com/how_to/) tutorials.

1. The ground of the virtual environment should be an imported mesh that is more complex that a simple rectangular ground plane. (2)
2. The environment should also contain *at least* six unique objects that are also imported meshes.  These objects should be placed in the environment to form a plausible scene.  (2)
3. The imported meshes should be children of a `TransformNode` object called `root`.  When you apply a transformation to the `root` node (e.g., moving or rotating), all the imported mesh objects in the scene should move along with it.  (1)
4. Add an ambient (hemispheric) light and a directional light.  Adjust the parameters for both lights so that the illumination looks reasonable in your scene.  (1)
5. Add a [skybox](https://doc.babylonjs.com/how_to/skybox) to the scene.  You can use the example textures from the Babylon website or find your own images on the internet.  (2)
6. Implement [collision detection](https://doc.babylonjs.com/babylon101/cameras,_mesh_collisions_and_gravity) so that the camera cannot fly through the mesh objects in your scene.  Note that you do not have to implement gravity, but you may choose to do so.  (1)
7. Build the program by executing `npm run build` and make sure to include your assets in the `dist` directory.  The debug layer should be disabled in your final build.  Upload it to your public `.www` directory, and make sure to set the permissions so that it loads correctly in a web browser.  You should include this URL in submission information section of your `README.md` file. (1)

**Bonus Challenge:**  Change to "night mode" when the `n` key is pressed.  In this mode, the ambient and directional lights should be made much darker to simulate an outdoor environment at night.  Add other types of lights that are only turned on at night, such as point and spot lights.  Adjust the parameters for these new lights to create some atmosphere in your scene.  When the `d` key is pressed, change back to "daytime mode" by returning all the lights to their original state. (1)

Make sure to document all third party assets. ***Be aware that points will be deducted for using third party assets that are not properly documented.***

## Submission

You will need to check out and submit the project through GitHub classroom.  The project folder should contain just the additions to the sample project that are needed to implement the project.  Do not add extra files, and do not remove the `.gitignore` file (we do not want the "node_modules" directory in your repository.)

**Do not change the names** of the existing files.  The TA needs to be able to test your program as follows:

1. cd into the directory and run ```npm install```
2. start a local web server and compile by running ```npm run start``` and pointing the browser at your ```index.html```

Please test that your submission meets these requirements.  For example, after you check in your final version of the assignment to GitHub, check it out again to a new directory and make sure everything builds and runs correctly.

## Local Development 

After checking out the project, you need to initialize by pulling the dependencies with:

```
npm install
```

After that, you can compile and run a server with:

```
npm run start
```

Under the hood, we are using the `npx` command to both build the project (with webpack) and run a local http webserver on your machine.  The included ```package.json``` file is set up to do this automatically.  You do not have to run ```tsc``` to compile the .js files from the .ts files;  ```npx``` builds them on the fly as part of running webpack.

You can run the program by pointing your web browser at ```https://localhost:8080```.

## Build and Deployment

After you have finished the assignment, you can build a distribution version of your program with:

```
npm run build
```

This project also includes a `deploy.sh` script that can automate the process of copying your assets to the `dist` directory, deploying your build to the web server, and setting public permissions.  To use the script, you will need to use a Unix shell and have`rsync` installed.  If you are running Windows 10, then you can use the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10).  Note that you will need to fill in the missing values in the script before it will work.

## License

Material for [CSCI 5619 Fall 2020](https://canvas.umn.edu/courses/194179) by [Evan Suma Rosenberg](https://illusioneering.umn.edu/) is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

The intent of choosing CC BY-NC-SA 4.0 is to allow individuals and instructors at non-profit entities to use this content.  This includes not-for-profit schools (K-12 and post-secondary). For-profit entities (or people creating courses for those sites) may not use this content without permission (this includes, but is not limited to, for-profit schools and universities and commercial education sites such as Coursera, Udacity, LinkedIn Learning, and other similar sites).   

## Acknowledgments

This assignment was based upon content from the [3D User Interfaces Fall 2020](https://github.blairmacintyre.me/3dui-class-f20) course by Blair MacIntyre.
