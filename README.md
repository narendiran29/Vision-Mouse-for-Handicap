# Vision-Mouse-for-Handicap
ABSTRACT  
Advancements in technology continue to revolutionize the way we interact with our devices, and one such 
innovation that holds immense potential for transforming accessibility is the development of an eye
controlled mouse. This groundbreaking project introduces a novel method of computer interaction, enabling 
individuals to navigate and operate their computers using only their eyes. By leveraging the capabilities of a 
camera to monitor facial movements, this system detects specific eye gestures such as blinks or controlled eye 
closures, translating them into mouse movements and clicks. What emerges is a seamless and intuitive 
interface that empowers users to interact with their computers hands-free, transcending the limitations 
imposed by traditional input devices . At its core, this eye-controlled mouse is a testament to the power of 
inclusive design. By catering to the needs of individuals with disabilities, it promotes inclusivity in 
technology, ensuring that everyone, regardless of physical limitations, can access and utilize digital resources 
with ease. For those who face challenges with conventional input methods due to motor impairments or other 
disabilities, this innovation represents a gateway to a world of possibilities. It provides a means of 
independent computer usage, granting users autonomy over their digital experiences and fostering a sense of 
empowerment . One of the key advantages of this eye-controlled mouse is its customizable sensitivity, 
allowing users to fine-tune the system according to their individual preferences and capabilities. This level of 
personalization ensures a tailored user experience, maximizing comfort and usability for each individual. 
Whether adjusting the sensitivity to accommodate subtle eye movements or refining the response time to suit 
specific needs, users have the flexibility to optimize their interaction with the technology.

INTROUCTION  
Introduction To Vision Mouse For Handicap 
In today's interconnected world, technology serves as a gateway to communication, 
education, employment, and social interaction. Yet, for individuals grappling with physical 
disabilities, the digital landscape often presents formidable barriers. Conventional input 
devices like keyboards and mice, while ubiquitous, can pose insurmountable challenges for 
those with limited mobility or dexterity. Recognizing this disparity, our project endeavors 
to bridge the gap through the development of the Vision Mouse for Handicap – an 
innovative solution poised to revolutionize computer interaction for individuals with 
disabilities. Our primary objective is clear: to empower individuals with physical 
disabilities to navigate their computers with unparalleled ease and precision using only 
their eyes. Leveraging state-of-the-art eye-tracking technology, our vision is to create a 
seamless interface that allows users to control the mouse cursor on their screen with 
unprecedented accuracy. By eliminating the need for physical input devices, the Vision 
Mouse for Handicap not only enhances accessibility but also fosters independence and 
autonomy for users, thereby enriching their overall quality of life. 

Open CV : 
Opencv is a huge open-source library for computer vision, machine learning, and image 
processing. Now, it plays a major role in real-time operation which is very important in 
today’s systems. By using it, one can process images and videos to identify objects, faces, 
or even the handwriting of a human. 
When it is integrated with various libraries, such as NumPy, python is capable of 
processing the opencv array structure for analysis. To Identify an image pattern and its 
various features we use vector space and perform mathematical operations on these 
features.  
The first OpenCV version was 1.0. OpenCV is released under a BSD license and hence it’s 
free for both academic and commercial use. It has C++, C, Python, and Java interfaces and 
supports Windows, Linux, Mac OS, iOS and Android. When opencv was designed the main 
focus was real-time applications for computational efficiency. All things are written in 
optimized C/C++ to take advantage of multi-core processing. 

MediaPipe Library : 
MediaPipe is an open-source framework for building pipelines to perform computer vision 
inference over arbitrary sensory data such as video or audio. Using MediaPipe, such a 
perception pipeline can be built as a graph of modular components. MediaPipe is currently in 
alpha at v0.7, and there may still be breaking API changes. Stable APIs are expected by v1.0. 
The MediaPipe framework is mainly used for rapid prototyping of perception pipelines with 
AI models for inferencing and other reusable components. It also facilitates the deployment 
of computer vision applications into demos and applications on different hardware platforms. 
The configuration language and evaluation tools enable teams to incrementally improve 
computer vision pipeline.

PyautoGUI Library: 
PyautoGUI library is an automation library that allows mouse and keyboard control. Or we 
can say that it facilitates us to automate the movement of the mouse and keyboard to establish 
the interaction with the other application using the Python script. It provides many features, 
and a few are given below. 
o We can move the mouse and click in the other applications' window. 
o We can send the keystrokes to the other applications. For example - filling out the 
form, typing the search query to browser, etc. 
o We can also take snapshots and give an image. 
o It allows us to locate a window of the application, and move, maximize, minimize, 
resizes, or close it. 
o Display alert and message boxes. 

Steps For Program: 
1. Initialize the video capture using cv2.VideoCapture(0) to access the default camera. 
2. Utilize the MediaPipe Face Mesh module (mp.solutions.face_mesh.FaceMesh) to 
detect facial landmarks in the captured frames. 
3. Retrieve the screen dimensions using pyautogui.size() to calculate the cursor position 
on the screen. 
4. Enter a while loop to continuously process video frames. 
5. Read a frame from the video capture using cam.read(). 
6. Flip the frame horizontally using cv2.flip(frame, 1) for correct orientation. 
7. Convert the frame to RGB color space using cv2.cvtColor(frame, 
cv2.COLOR_BGR2RGB). 
8. Process the RGB frame with the Face Mesh model using 
face_mesh.process(rgb_frame). 
9. Retrieve the facial landmark points from the output using 
output.multi_face_landmarks. 
10. Calculate the screen coordinates based on the position of specific facial landmarks. 
11. Move the cursor to the calculated screen coordinates using 
pyautogui.moveTo(screen_x, screen_y). 
12. Detect left eye blinks by comparing the vertical positions of specific landmarks. 
13. If the difference in vertical positions falls below a threshold, simulate a mouse click 
using pyautogui.click(). 
14. Show the processed frame with overlaid facial landmarks and eye blink detection 
using cv2.imshow(). 
15. Wait for a key press using cv2.waitKey(1).

 CONCLUSION  
In conclusion, the virtual mouse system developed in this project signifies a groundbreaking 
advancement in assistive technology, particularly for individuals with physical disabilities. By 
harnessing the power of eye movement captured through a webcam, this system offers a 
revolutionary hands-free solution for computer interaction. The capability to control the 
mouse cursor with precision and ease empowers users to navigate digital environments with 
newfound independence and efficiency. The system's innovative approach to accessibility 
addresses a critical need in the realm of technology, paving the way for greater inclusivity. By 
eliminating the reliance on traditional input devices, such as keyboards and mice, individuals 
with physical disabilities can overcome barriers that previously hindered their full 
participation in digital activities. This breakthrough holds immense potential to enhance the 
quality of life for countless individuals by providing them with the tools to engage more fully 
in various aspects of daily life, including communication, education, work, and entertainment.

FUTURE WORK  
1. Enhanced Gesture Recognition: Continuously refine gesture recognition algorithms to 
expand support for a wider range of eye movement and actions. This could involve 
incorporating machine learning techniques to improve accuracy and robustness in detecting 
and interpreting various hand movements. 
2. Advanced Customization: Explore opportunities to expand customization options within 
the system, allowing users to personalize their experience further. This may include additional 
parameters for sensitivity, gesture mapping, and interface customization to accommodate 
diverse user preferences and needs. 
3. Integration with Assistive Technologies: Investigate possibilities for integrating the 
virtual mouse system with other assistive technologies and devices. This integration could 
enhance accessibility and functionality by leveraging complementary technologies such as 
speech recognition, switch access, or brain-computer interfaces to provide alternative input 
methods and expand the system's capabilities. 
4. User Feedback and Iterative Improvements: Implement a robust feedback mechanism to 
gather user input and insights continually. User feedback should inform iterative 
improvements to the system's design and implementation, addressing usability issues, refining 
features, and enhancing overall performance based on real-world usage scenarios.
