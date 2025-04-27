# cs6476-problem-set-5--object-tracking-and-pedestrian-solved
**TO GET THIS SOLUTION VISIT:** [CS6476 Problem Set 5- Object Tracking and Pedestrian Solved](https://www.ankitcodinghub.com/product/cs6476-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;123845&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS6476 Problem Set 5- Object Tracking and Pedestrian Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
Problem Set 5: Object Tracking and Pedestrian

Detection

ASSIGNMENT DESCRIPTION

Description

In Problem set 5, you are going to implement tracking methods for image sequences and videos. The main algorithms you will be using are the Kalman and Particle Filters. Methods to be used: You will design and implement a Kalman and a Particle filters from the ground up.

Refer to this problem set’s autograder post for a list of banned function calls.

Please do not use absolute paths in your submission code. All paths should be relative to the submission directory. Any submissions with absolute paths are in danger of receiving a penalty!

LearningObjectives

• Identify which image processing methods work best in order to locate an object in a scene.

• Learn to how object tracking in images works.

• Explore different methods to build a tracking algorithm that relies on measurements and a prior state.

• Create methods that can track an object when occlusions are present in the scene.

StarterCode

Obtain the starter code from canvas under files.

INSTRUCTIONS

ProgrammingInstructions

Your main programming task is to complete the functions described in the file PS5.py. The driver program experiment.py helps you illustrate the results and will output the files needed for the writeup.

Write-upInstructions

Create ps5_report.pdf – a PDF file that shows all your output for the problem set, including images labeled appropriately (by filename, e.g. ps5-1-a-1.png) so it is clear which section they are for and the small number of written responses necessary to answer some of the questions (as indicated). You are required to use do the following when creating your report:

• Use the LATEX template provided.

HowtoSubmit

Two assignments have been created on Gradescope: one for the report – PS5_report, and the other for the code – PS5_code.

• Report: the report (PDF only) must be submitted to the PS5_report assignment.

• Code: all files must be submitted to the PS5_code assignment. DO NOT upload zipped folders or any sub-folders, please upload each file individually. Drag and drop all files into Gradescope.

note:

Notes

• If you wish to modify the autograder functions, create a copy of those functions and DO NOT mess with the original function call.

Grading

The assignment will be graded out of 100 points. The code portion (autograder) represents 75% of the grade and the report the remaining 25%.

ASSIGNMENT QUESTIONS

1 THE KALMAN FILTER

The Kalman Filter (KF) is a method used to track linear dynamical systems with gaussian noise. Recall that both the predicted and the corrected states are gaussians, allowing us to keep the mean and covariance of the state in order to run this filter. Use the kalman filter on the provided images to track a moving circle.

First we need to define the KF’s components. We will use the notation presented in the lectures for the N-dimensional case.

State vector:

We represent the filter’s state using the current position and velocities in the x, y plane. We will not use acceleration in our exercise.

X = [x,y,vx,vy]

Dynamics Model transition 4×4 matrix Dt :

This matrix will map the equations below to the state components. Determine how this 4×4 matrix can be used to represent these equations using the state vector.

xt = x(t −1)+vx∆t yt = y(t −1)+vy∆t

∆t = 1 for simplicity

State and Covariance prediction:

We assume that the state vector prediction is based on a linear transformation using the transition matrix Dt. And the covariance is obtained from the squaring operation plus the process noise Σdt .

We will also assume this noise is independent from each component in the state vector.

Xt− =DtXt+−1

Σ−t =DtΣ+t−1DTt +Σdt

σ2dx

 0

Σdt 0





0 0

σ2dy

0 0 0 0

σ2dvx

0 0 

0 

 0 

σ2dvy 

Before we continue to the Correction state. We will define our sensor’s function as a way to obtain the object’s position. In our case we will use a template matching code to obtain these components. In order to make this a little more interesting, we will add some noise to these measurements.

Sensor measurement 2×4 matrix Mt:

This matrix maps the available measurements to the state vector defined above. Because we can only obtain two values, x and y, it contains two rows and four columns.

Kalman Gain Kt :

Using the measurement matrix, and the predicted covariance we can now compute the Kalman Gain. Here you will also define a measurement noise represented by Σmt .

Kt =Σ−t MtT(MtΣ−t MtT +Σmt )−1

State and Covariance correction:

Now that we have all the components we need, you will proceed to update the state and the covariance arrays. Notice that in order to update the state you will use the residual represented by the difference between the measurements obtained from the sensor (template matching function) Yt and the predicted positions MtXt−.

Xt+ = Xt−+Kt(Yt −MtXt−) , where Yt is the measurements at time t Σ+t = (I −KtMt)Σ−t , where I is the identity matrix

In the next iteration the updated state and covariance will be used in the prediction stage.

Initialize the class defining the class arrays you will be using. Place these components in the _init_(sel f ,init_x,init_y) function.

Here’s a reminder of what should be included in this part:

• State vector (X) with the initial x and y values.

• Covariance 4×4 array (Σ) initialized with a diagonal matrix with some value.

• 4×4 state transition matrix Dt

• 2×4 measurement matrix Mt

• 4×4 process noise matrix Σdt

• 2×2 measurement noise matrix Σmt

Code: __init__(self, init_x, init_y)

Complete the prediction state in predict(self). Here you will replace the class variables for the state and covariance arrays with the prediction process.

Code: predict(self)

Finally, we need to correct the state and the covariances using the Kalman gain and the measurements obtained from our sensor.

Code: correct(self)

b.

The position estimation is performed by the function process(self, measurement_x, measurement_y) which uses the functions defined above. Now that you have finished creating the Kalman Filter, estimate the position of a bouncing circle. Use the images in the directory called ‘circle’ to find the circle’s position at each frame.

Input: circle/0000.jpg to circle/0099.jpg. Code: part_1b()

c.

Now let’s try with a more complicated scene using the same filter. We will find and track pedestrians in a video. This means we need to update our sensor with a function that can locate people in an image. Fortunately, there is a function in OpenCV that can help us with this task using Histogram of Gradients (HoG) descriptors. This object contains a method called detectMultiScale that returns the bounding boxes for each person in the scene along with the detection weight associated to it.

Use the sequence of images in the ‘walking’ directory to detect and follow the man crossing the street using the output from the HoG detector as the measurements and the Kalman Filter.

Input directory: walking/001.jpg to walking/159.jpg

Code: part_1c()

2 THE PARTICLE FILTER

Recall that we need a variety of elements:

1. a model – this is the “thing” that is actually being tracked. Maybe it’s a patch, a contour, or some other description of an entity;

2. a representation of state xt that describes the state of the model at time t;

3. a dynamics model p(xt|xt−1) that describes the distribution of the state at time t given the state at t-1;

4. a measurement zt that somehow captures the data of the current image; and finally, 5. a sensor model p(zt|xt) that gives the likelihood of a measurement given the state. For Bayesian-based tracking, we assume that at time t-1 we have a belief about the state represented as a density p(xt−1), and that given some measurements zt at time t we update our Belief by computing the posterior density: Bel(xt) ∝ p(zt|xt)p(xt|ut,xt−1)Bel(xt−1)

In class we discussed both the theory and the implementation specifics behind particle filtering. The algorithm sketch is provided in the slides and it describes a single update of the particle filter. What is left up to the coder are several details including what is the model, what is the state, the number of particles, the dynamics/control function p(xt|xt−1,ut), the measurement function p(zt|xt), and the initial distribution of particles.

For this question, you will to need track an image patch template taken from the first frame of the video. For this assignment the model is simply going to be the image patch, and the state will be only the 2D center location of the patch. Thus each particle will be a (u, v) pixel location (where u and v are the row and column number respectively) representing a proposed location for the center of the template window.

We will be using a basic function to estimate the dissimilarity between the image patch and a window of equal size in the current image, the Mean Squared Error:

MSE(up,vp) = mn1 Pmu=1Pnv=1(Template(u,v)−Imaget(u+up − m2 ,v +vp − n2 ))2

The funny indexing is just because (u, v) are indexed from 1 to M (or N) but the state (up,vp) is the location of the center. Notice the above equation can be simplified by using array operations. Remember you are calculating the Mean of the Squared Error between two images, a template and a patch of the image.

These images are color and you will convert them to grayscale can do the tracking in either the full color image, or in grayscale, or even in the green channel. If you use color, there would be an outer summation over the three color channels. If you want to use grayscale, you can use cvtColor in OpenCV or just use a weighted sum of R,G,B to get a luma value (try weights of 0.3, 0.58, and 0.12).

MSE, of course, only indicates how dissimilar the image patch is, whereas we need a similarity measure so that more similar patches are more likely. Thus, we will use a squared exponential equation (Gaussian) to convert this into a usable measurement function: p(zt|xt) MSE

To start out, you might use a value of σMSE = 10 (for grayscale in 0-255 range) but you might need to change this value.

For the dynamics we’re going to use normally distributed noise since the object movements can be unpredictable and often current velocity isn’t indicative of future motion; so our dynamics model is merely xt = xt−1+δt, where δtisN(0,Σd),Σd = ·σ0d2 σ02d¸

which is just a fancy way to say you add a little bit of Gaussian noise to both u and v independently.

In order to visualize the tracker’s behavior you will need to overlay each successive frame with the following elements:

• Every particle’s (x,y) location in the distribution should be plotted by drawing a colored dot point on the image. Remember that this should be the center of the window, not the corner.

• Draw the rectangle of the tracking window associated with the Bayesian estimate for the current location which is simply the weighted mean of the (x,y) of the particles.

• Finally we need to get some sense of the standard deviation or spread of the distribution. First, find the distance of every particle to the weighted mean. Next, take the weighted sum of these distances and plot a circle centered at the weighted mean with this radius.

You are encouraged to produce these visuals for selected frames. You will not have to submit the entire video.

For reading the frames OpenCV users should look at the class VideoCapture. For sampling based on a distribution, see the functions numpy.random.multinomial or numpy.random.choice. a.

Implement the particle filter. You can find the bounding box for the initial position in template_rect – this is your template. Tweak the parameters including window size until you can get the tracker to follow this object. Run the tracker and save the video frames described below with the visualizations overlaid.

Classes, methods: Define a class ParticleFilter, with the following methods:

• _init_(f rame,template,∗∗kwargs) : (constructor) Initialize particle filter object.

• get_error_metric(template, f rame_cutout) : Calculates the error metric used (i.e. MSE).

• resample_particles() : Returns a list of particles resampled based on their weights.

• process(f rame) : Process a frame (image) of video and update filter state.

* Hint: You should call resample_particles() and get_error_metrics() here.

• render(f rame_out) : Visualize current particle filter state.

Finally, modify the variables num_particles, sigma_mse, sigma_dyn in the part_2a() function to appropriate values.

A helper function, run_particle_f ilter(), has been provided to run your particle filter on a video. You can also display every video frame to verify that your particle filter is working properly.

Note: The helper function run_particle_f ilter() can save the template image patch and outputs generated by your render() method for desired frames. See template code for details.

Input directory: circle/0000.jpg to circle/0099.jpg Code: ParticleFilter() and part_2a() in ps5.py

b.

Now use the particle filter with a noisy video sequence of images in the ‘pres_debate_noisy’ directory.

Input directory: pres_debate_noisy/000.jpg to pres_debate_noisy/099.jpg

Code: part_2b() in ps5.py

3 CHANGES IN APPEARANCE

In the last section you were working with a static template assuming that the target will not change in shape. This can be addressed by updating the model’s appearance over time.

Modify your existing tracker to include a step which uses the history to update the tracking window model. We can accomplish this using what’s called an Infinite Impulse Response (IIR) filter. The concept is simple: we first find the best tracking window for the current particle distribution as displayed in the visualizations. Then we just update the current window model to be a weighted sum of the last model and the current best estimate. Template(t) =αBest(t)+(1−α)Template(t −1)

a.

Implement the appearance model update feature. Run the tracker on the presidential debate images and adjust parameters until you can track the person’s hand (the one not holding the microphone). Your tracker’s bounding box should only contain the hand at all times. Run the tracker. You can save the video frames with the visualizations overlaid for reference.

Classes, methods: Derive a class AppearanceModelPF from ParticleFilter, retaining the same interface – i.e., with methods process() and render(), as defined above. The constructor and process() method should transparently handle model updates. You can supply additional keyword arguments to the constructor, if needed.

Finally, modify the variables num_particles, sigma_mse, sigma_dyn in the part_3() function to appropriate values

Input directory: pres_debate/000.jpg to pres_debate/165.jpg

Code: AppearanceModelPF() and part_3() in ps5.py

4 PARTICLE FILTERS AND OCCLUSIONS

For this part we will work with a much more difficult video to perform tracking with, pedestrians.mp4. We’d like to be able to track the blond-haired woman (the one with the white jacket) as she crosses the road. If you try applying your adaptive tracker to this video, you will probably find that you will have difficulty dealing simultaneously with occlusion and the perspective shift as the woman walks away from the camera. Thus, we need some way of relying less on updating our appearance model from previous frames and more on a more sophisticated model of the dynamics of the figure we want to track.

Expand your appearance model to include window size as another parameter. This will change the representation of your particles. You are highly recommended to use cv2.resize for your implementation to resize the template to track.

a.

Run the tracker and save the video frames described below with the visualizations overlaid. You will receive full credit if you can reliably track (illustrate this with the rectangle outline) all the way to the end of the street and deal gracefully with the occlusions (reasonable tracking at frame 300). The tracking box must track the person’s position and size. The bounding box is expect to contain more than 50% of the tracked person and should be within 0.5 times to 2 times the size of the person.

Classes, methods: Derive a class MDParticleFilter from AppearanceModelPF, retaining the same interface – i.e., with methods process() and render(), as defined above. The constructor and process() method should transparently handle model updates in appearance and dynamics. You can supply additional keyword arguments to the constructor and other methods, if needed.

Finally, modify the variables num_particles, sigma_mse, sigma_dyn in the part_4() function to appropriate values.

Code: MDParticleFilter() and part_4() in ps5.py Report: Frames to record 40, 100, 240, 300.

-Input: pedestrians/000.jpg to pedestrians/319.jpg.

-Output: ps5-4-a-1.png, ps5-4-a-2.png, ps5-4-a-3.png, and ps5-4-a-4.png

-Text Answer: Describe what you did. How did you modify the Particle Filter class to continue tracking after occlusions?

5 TRACKING MULTIPLE TARGETS

Now use either a kalman or particle filter to track multiple targets as they move through the given video. Use the sequence of images in the TUD-Campus directory to detect the people shown below. The bounding box is expect to contain more than 50% of the tracked person and should be within 0.5 times to 2 times the size of the person.

Input directory: TUD-Campus/01.jpg to TUD-Campus/71.jpg Code: part_5() in experiment.py Report:

– Frames to record: 29, 56, 71

– Output: ps5-5-a-1.png, ps5-5-a-2.png, ps5-5-a-3.png

– Text Answer: Describe what you did. How different it was to use a KF vs PF? Which one worked best and why? Include details about any modifications you had to apply to handle multiple targets.

6 DETECT PEDESTRIANS FROM A MOVING CAMERA

Finally, detect pedestrians from the given video of a moving camera. Use the images in the directory ‘follow’ to track the man with the hat holding a white plastic bag. Similar to earlier tasks, the bounding box is expect to contain more than 50% of the tracked person and should be within 0.5 times to 2 times the size of the person.

Input directory: follow/001.jpg to follow/186.jpg Code: part_6() in experiment.py Report:

– Frames to record: 60, 160, 186

– Output: ps5-6-a-1.png, ps5-6-a-2.png, ps5-6-a-3.png

– Text Answer: Describe what you did. Did this task present any additional challenges compared to the previous sections? Include details about any modifications you had to apply.
