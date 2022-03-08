# OpenGL Hands On Practice

## 陈胤良202030000403

---

## Windows10+VS2019+OpenGL Installation

1. Download the GLUT from the website:
   [https://www.opengl.org/resources/libraries/glut/glut_downloads.php](https://www.opengl.org/resources/libraries/glut/glut_downloads.php)
   we wish to download the header file glutdlls37beta.zip
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/GLUT.png "")
   then unzip the glutdlls37beta.zip file, we will get the following files:
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/GLUTdlls.png "")

2. Next, we neet to create a new folder named gl in
   `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\VS\include`
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/folder.png "")

3. Paste the glut.h file in 
   `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\VS\include\gl`
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/header.png "")

4. Paste the glut.lib library in
   `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\VS\lib\x64`

   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/lib.png "")

5. Paste the glut32.lib library in
   `C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\VS\lib\x86`
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/lib32.png "")

6. Paste the glut.dll and glut32.dll dynamic libraries in
   `C:\Windows\SysWOW64`
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/dlls.png "")

7. Finally, paste the glut32.dll in
   `C:\Windows\System32 `
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/dll.png "")

### Errors Occurred:

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/error1.png "")

### Solution:

1. In Visual Studio 2019 GUI：

   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/solution1.png "")

2. Select **Zi** instead of **ZI**
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/solution2.png "")

3. Choose Yes/Gy and click apply
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/solution3.png "")

4. Successfully sovled the issue and obtained the output
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/success.png "")
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/testoutput.png "")

---

## 3D Sierpinski Gasket Volume Division Experiment

### Configuration Process

1. Download the zip file from group file station:
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/test.png "")
2. Unzip the zip file and open the .sln project file using Visual Studio 2019
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/test2.png "")
3. Build solution and run, any error occurred, see [Errors Occurred:](https://www.wolai.com/vDbFMwfVwt9rXUdVkCybdC)
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/test3.png "")
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/test4.png "")
4. Output the solution
   ![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/output.png "")

### Tuning Parameters:

#### Modify Sierpinski Gasket subdivision steps:

n=4

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/n4.png "")

n=8

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/n8.png "")

n=6

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/n6.png "")

n=10

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/n10.png "")

I feel that as the subdivision steps increses, the feeling of a 3D graph decreases

#### Modify GLUT_DEPTH option:

Without GLUT_DEPTH

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/nodepth.png "")

With GLUT_DEPTH

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/depth.png "")

There is no obivious difference between with and without GLUT_DEPTH option, which was strange.

I made one assumption that when performing Volume Division, GLUT_DEPTH option is set as default. (Confirmed with Ms.Xiao that the latest OpenGL library indeed set this to default)

Then I tired removing GLUT_DEPTH in Surface Division and got the following results:

Without GLUT_DEPTH

With GLUT_DEPTH

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/surface2.png "")

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/surface1.png "")



It worked for surface division, which shows that this has something to do with the code.

And I found that I forgot to remove glEnable(GL_DEPTH_TEST) when performing the test in Volume Division.

I tried again with GL_DEPTH_TEST off, the results are as follows:

#### Removing glEnable(GL_DEPTH_TEST):


![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/disabel.png "")

We can see that after removing the GL_DEPTH_TEST option, the output images look more like a 2D images rather than a 3D images.

#### Messing with colors:

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/colors.png "")

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/colors3.png "")

![images](https://github.com/cylqqqcyl/ComputerVisionOpenGL/blob/main/OpenGLInstallation%26FirstExperiment/images/colors2.png "")

Fun and relaxing.

---

### Feelings

Realling amazing OpenGL basic hands on practice, allowed me to get to know some OpenGlL functions, which was really cool.

Not a rough part for me to set up the environment or compile the code, went on smoothly.

Occurred some errors during the process, but they weren't hard to solve.

Gained a great sense of achievement when seeing the beautiful output results.

Made some assumptions when tuning the parameters.

Enjoyed.
