# Form Code Snapshots to Runnable Programs
This idea was first invented and disclosed in December 2018, as part of participation at a Hackathon hosted by GitHub, in which we achieved 2nd place.

_Disclaimer: A prototype was developed as a proof of concept for the idea by a team of four students formed to participate in the Hackathon. However, I, Taher Ghaleb, was the main author of the idea._

## Abstract
**Background.** Programs of any programming language produce a certain output from a set of instructions (i.e., source code). Every program instruction has predefined syntax and semantics. Running a program requires either a compiler (to check all at once code and generate machine code) or an interpreter (to check and generate machine code instruction by instruction), depending on the programming language. For example, the Java programming language uses compilers, whereas Python uses interpreters.

**Motivation.** Using a compiler/interpreter could be straightforward if a soft copy of the program source code is available (i.e., code is written and stored in a source file). However, a soft copy of the source code might not always be available. For example, computer science students/teachers may encounter source code in reading textbooks, tutorials, lecture slides/notes, or exam/assignment sheets. It is also typical to encounter program source code written on whiteboards/blackboards while giving class lectures or coding interviews. In such cases, converting the hard-written code into runnable soft-written code may not be effective, since it could be time-consuming and prone to human mistakes. In addition, even if the code is soft-written, it might represent only partial functionality of a program or contain errors. Therefore, running such code would generate the output.

**Aim.** This invention aims to apply machine learning to run programs in which code is hard-written, incomplete, or erroneous and produce a timely output.

**Invention.** The invented solution allows to (1) read programming source code from any source using a camera, (2) convert such code into compute-readable code, (3) fix any potential errors, (4) run the code using an appropriate compiler/interpreter, (5) generate output, and (6) display the output to a screen.

## Background material
Using a camera to process hard-written text is supported by some existing products, such as Google Translate. The Google Translate mobile application allows users to use a phone’s camera to point to any text written on surrounding objects and generates the translation of such text into other preferred languages. To do so, the Google Translate application uses an Optical Character Recognition (OCR) technology that transforms texts from images into computer-readable text. However, existing OCR technologies only support the text of natural languages. For example, an OCR technology could miss or misinterpret whitespaces or special characters, such as parentheses or semicolons. Whitespaces and special characters play a vital role in programming languages, since they are part of the syntax. 

## Design alternatives:
The invention could be designed and developed as:
 - A mobile application in which the phone’s camera could be used to take pictures of program source code and then process the code accordingly.
 - A code-reader-runner device that has a camera, processor, memory, storage, internet, etc.

## Invention architecture
Figure 1 presents a flowchart that shows how the invention works. The first step of the invented solution starts with a user having a code snippet written on some object. The front-end employs a camera that receives an image of the code and sends such an image to the backend. The backend processes such an image by (i) converting the code on the image to computer-readable code, (ii) checking whether the code is incomplete or erroneous, (iii) running the code on a compatible compiler/interpreter, and (iv) generating and sending to the frontend. The front-end then sends the output. Such a process could be interactive in such a way the code might not generate a single output. For example, the code may contain repetitions (i.e., loops) that lead to generating repetitive output or may require the user’s input at runtime. 

  <figure>
    <img width="80%" align="center" alt="Figure 1. A flowchart of how the invention works" src="https://user-images.githubusercontent.com/25190974/162706731-489321d3-56ee-4838-a6cb-10746fbdbcac.png">
      <figcaption><i>Figure 1. A flowchart of how the invention works</i></figcaption>
  </figure>

## Proposed Features
 - Improve the code recognition accuracy using Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs)
 - Detect which programming language the code is written with
 - Allow programmers to fix or modify the code after code generation
 - Show the documentation of a specific part of the code (e.g., a class or function) using online resources.
 - Deal with lengthy output produced on the console (e.g., in case of loops or tracing).
 - Deal with GUI (i.e., returning the GUI of a code and making it interactive from mobile)
 - Anomaly detection after running the code, by leveraging GitHub or Stack Overflow, e.g., code security vulnerability, code recommendation based on running error or warning.
 - Fix errors and autocompleting partial programs using clone detection approaches by leveraging online resources of source code (e.g., [GitHub](https://github.com) and [Stack Overflow](https://stackoverflow.com).

## Prototype
A prototype of the invention was developed as an Android mobile app. Images were collected from a phone’s camera, including Java code written on a computer screen, blackboard, textbook, and handwritten. The data include images that are of good and bad quality to better train the model. The prototype employed an open-source Application Programming Interface (API) called [opencv](https://github.com/opencv/opencv) to enhance the quality of images and reduce noise. Then, the enhanced images were use to convert the scanned code into computer-readable code using the text recognition function of an open-source API called [tesseract](https://github.com/tesseract-ocr/tesseract). The prototype is aimed to be improved int eh future to use deep learning models, trained on millions of code snippets available online, to identify whether the generated code contains syntax errors or if the code is partial (i.e., requires completion to run properly). Then, the generated code is run using an open-source online compiler API called [judge0](https://github.com/judge0/judge0). The output returned from the online compiler is synchronize with the mobile application to be displayed on the phone’s screen.

## Stakeholders:
 - Publishers of programming language textbooks: the invention can be provided as an add-on with textbooks to help produce output from the written code snippets.
 - Institutions (e.g., schools, colleges, universities, etc.): the invention can be provided for (a) instructors to help mark coding exams/assignments and (b) students to help understand the output of code when written on boards, textbooks, or slides.
 - Tech companies: the invention can be used by tech companies when conducting coding interviews with job applicants.

## Contributions.
If you are interested in contributing to this project, please send an email to [Taher Ghaleb](mailto:taher.a.ghaleb@gmial.com). Thank you for your interest.
