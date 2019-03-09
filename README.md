# computer_vision_demonstrator
This project will use a Qt GUI to demonstrate various "traditional" computer vision techniques to the user.

Brainstorming:

  * Libraries used:
      - OpenCV 3.X
      - Qt 5.12
      - Boost 1.68 ?
      - ?

  * Graphical User Interface:
      - Choose image to process
      - Choose image processing (IP) technique (from drop-down menu?)
      - Set relevant parameters using input text boxes and sliders
      - See output / result image
      - Chain multiple IP techniques together --> using linear sequence of IP techniques as part of process
      - Run / Stop program

  * Command-Line User Interface:
      - performs similarly to GUI, but only provides relevant information
      - lists possible IP techniques on CLI
      - user can choose GUI or CLI
      - provides user with basic debugging / running info on CLI

  * Under-the-hood:
      - 1 thread for user interface
      - remaining threads for IP steps
      - reads-in image
      - particular technique is performed, based on chosen IP technique(s)
      - reads-in IP technique settings / values
      - performs IP technique
      - sends resulting image to GUI / CLI
      - waits for user to request next IP technique?
      - sends error message(s) to GUI / CLI if IP technique cannot be performed
      
  * Software Engineering:
      - Testing:
          ~ Unit Tests: google test
          ~ Unit Tests: Qt Test
          ~ Valgrind?
          ~ Coverage?
          ~ Integration tests
          ~ etc.
      - Version control:
          ~ git
      - Issue tracking:
          ~ JIRA?
      - Building:
          ~ CMake?
          ~ qmake?
      - Continuous Improvement?
      - Code Reviews from peers?
      
Customer Needs:
  * Customer: (Me)
      - I want to demonstrate knowledge of various image-processing and computer-vision techniques
      - I want to demonstrate knowledge of various Qt Libraries
      - I want to demonstrate knowledge of various OpenCV Libraries
      - I want to demonstrate knowledge of various Multithreading and IPC techniques (depending on what I need)
      - I want a user-friendly application that I can show to my parents and they can understand how to use it
      - I would like this application to be useful to show what various techniques do to a given image
      - I would like this application to be able to process any (reasonably-sized) image in under a minute.
      - I would like this application to be able to perform as many IP techniques / CV techniques on an image as I (the user) select from the menu.
      
  * Requirements:
      - Must be written in C++
      - Must use OpenCV with C++
      - Must use Qt with C++
      - Must use Modern C++ techniques wherever relevant (C++11/14/17)
      - Must have useful and self-documenting variable names
      - Must have comments for any novel sections of code
      - Must have comments for any 3rd-Party Library sections of code (OpenCV, Boost)
      - Must use at least 2 threads (1 for GUI/CLI and 1 for CV/IP BTS)
      - Must return a result (image or error statement(s)) for each process attempted
      - Must have relevant tests covering all edge cases for each process
      - Should test as many combinations of CV/IP techniques as possible --> quality of combinations is left to the user to assess (The user: "Was this a good idea?" vs. The program: "Was the result an image at all?")


Additional Notes:
  * Might need to split this into two programs / sections of one larger program:
      - image processing
      - computer vision (on post-processed images?)
  * Possible steps in scaling-up demonstrator:
      0) Download Qt Creator
      1) Download & Build OpenCV 3 from source
      2) Create basic UI
      3) Create basic program
          - overwrite basic image with constant pixel value?
          - convert color image to grayscale?
          - convert color image to HSV / etc. color image?
      4) Write tests for basic program
      5) Split program into 2 threads
          - 1 thread for UI
          - 1 thread for image processing / computer vision
      6) Write tests for multithreaded basic program
      7) Add 2nd technique to multithreaded basic program
      8) Test 2nd technique
      9) <REPEAT> Add additional IP/CV techniques, writing tests for each
      10) ?
  
  


      
      
      
      
