java c ENGF0004 Mathematical Modelling and Analysis II 2024/2025 Coursework 1 Release Date: 18 November 2024 Submission Deadline: 6 January 2025, 2 pm UK time Estimated Coursework Return: 4 working weeks after deadline Topics Covered: Topics 1 - 4 Expected Time on Task: 20 hours Guidelines: Failure to follow this guidance might result in a penalty of up to 10% on your marks. I. Submit a single PDF document with questions in ascending order. This can be produced for example in Word, LaTeX or MATLAB Live Script. Explain in detail your reasoning for every mathematical step taken. Include units for final answers where possible. II. Do not write down your name, or student number, or any information that might help identify you in any part of the coursework. Do not write your name or student number in the title of your coursework document file. Do not copy and paste the coursework questions into your submission - simply rewrite information where necessary for the sake of your argument. III. Insert relevant graphs or figures, and describe any figures or tables in your document. All figures must be labelled, with their axes showing relevant parameters and units. IV. You will need MATLAB coding to solve some questions. Include all code as pasted text in an Appendix at the end of your document. Remember to comment on your code, explaining your steps. This coursework is worth a total of 100 marks and counts towards 20% of your final ENGF0004 grade. Coversheet Please complete this coversheet to declare you have followed good academic practice. Please tick the boxes that apply.

I have carefully read and understood Section 9 of the academic manual: Student AcademicMisconduct Procedure https://www.ucl.ac.uk/academic-manual/chapters/chapter-6-student-casework-framework/section-9-student-academic-misconduct-procedure. Yes 口 No 口
I have made sure to correctly reference external resources incl. any teaching material. Yes 口 No 口
Have you used any AI tools to support your assignment? Yes 口 No 口
If so, which one(s)?
Answer:
I have made sure to correctly reference the use of any AI tools in the entirety of my report. Yes 口 No 口 Declaration I declare that all the information provided is true and understand that failure to comply with section 9 of the academic manual may result in penalties as outlined. to sign>
Learning Objectives
Skills in Mathematical Modelling and Analysis Figure 1. Key stages in mathematical modelling. As part of this module, throughout the core learning activities, workshops and courseworks , we aim to equip you with the essential skills in mathematical modelling and analysis. The process of mathematical modelling can be, for instance, broken down in three key stages, which we hope become part of your skill set in your studies and career going forward. The three stages are shown in Figure 1. During the first stage, the analytical model is set up. This includes employing the relevant simplifying assumptions, identifying main variables and parameters. To do this, the relevant literature needs to be researched to understand the main theory used to explain the phenomenon under consideration and what physical laws govern it. In the second stage, this model is implemented computationally. In this stage, the model can be allowed additional complexity if numerical solution methods are going to be employed. Important in this stage is making sure the model is behaving as expected, through sensitivity analysis and validation. The sensitivity analysis also allows us to identify the most important parameters that determine the behaviour of the system. After this we are ready to use our model to obtain new and useful information. We can change parameters and operating (boundary or initial) conditions to predict the way the system will behave in new conditions. We can use this simulation to design the properties of the system for a required application, or understand how to operate the system to make it more efficient or durable. Keep this framework of skills in mind for the duration of this module as one of the main learning outcomes you want to obtain at the end.

Detailed Learning Objectives

Apply a technique: Separation of variables method to reduce PDEs to ODEs.

Apply a technique: General solution of ODEs through the auxiliary equation.

Apply a technique: Apply initial and boundary conditions appropriately to find a particular solution to the ODEs and PDE.

Apply a technique: Laplace transforms and inverse Laplace transforms to solve ODEs.

Apply a technique: Represent a periodic function using Fourier Series.

Model computationally: Implement computationally solutions for system behaviour.

Model computationally: Implement a computational algorithm to solve a PDE using finite difference methods.

Model computationally: Perform a sensitivity analysis to understand effect of model parameters. Communicate technical information: Present clearly and concisely theoretical or computational methods used to study a system. Use clear and labelled graphs to assist in this communication by displaying solutions or other key points.

Show an understanding of a physical problem and an ability to interpret it mathematically.

Show an understanding of the implications of mathematical results about the behaviour of the system.

Show an understanding of the impact of model parameters on system behaviour. Model: Oscillation of Bridge Structures [100%]

Figure 2. Millennium Bridge in London.
Introduction The increasingly slender design of modern footbridges results in a reduced natural frequency of their structure. This reduced natural frequency, in turn, causes a higher sensitivity of the structure to dynamic forces induced by pedestrians, because the natural frequency of the structure drops into the range of frequencies of human walking , of order of approximately 1 Hz. Such bridges are in danger of becoming unstable, particularly in the lateral direction, when large crowds walk on the bridge. Such a phenomenon was observed when the Millennium Bridge was opened to the public on 10 June 2000. The first pedestrians experienced alarming swaying motion which led to the closure of the bridge for two years, until modifications by adjusting the bridge’s damping were made. In this coursework, this problem will be studied through a simplified dynamic model of a similar pedestrian bridge. Developing a mathematical model to study the lateral vibrations of a bridge The movement of the bridge platform in the lateral direction (sideways), fa代 写ENGF0004 Mathematical Modelling and Analysis II 2024/2025 Coursework 1R 代做程序编程语言r from its supports, under the action of the periodic force resulting from pedestrians walking , is graphically depicted in Figure 3. This lateral deflection can be modelled by the well-known second order ordinary differential equation representing the damped oscillation of a spring-mass system (E1) m + c + kx = r(t), (E1) where Table 1. Table of model parameters and coefficients.
Variable Value Description m 1 × 105 kg mass of the bridge platform x(t) [m] lateral displacement, measured in [m] c 12 × 105 kg/s damping coefficient of the bridge k 36 × 105 kg/s2 stiffness of the bridge r(t) [N] force in the lateral direction from pedestrians walking G 30 N Magnitude of average lateral force, r(t) , on the bridge from one person N

Number of pedestrians on the bridge f 1 Hz Gait lateral frequency

Figure 3. A schematic representation of a bridge as a spring-mass-dampener system to model vibrations
resulting from pedestrians walking. STAGE 1: Analytical Model [65 marks]
The following questions will help you set up and solve the analytical model, hence they will be more prescriptive in direction. Question 1 [30 marks]
a) [5] Determine the natural frequency of oscillation of the bridge , wn. Remember, this assumes the bridge oscillates freely and there is no damping. b) [10] Solve the governing equation (E1) using Laplace transforms to find the response of the system if r(t) = sin(2πt) . The initial conditions are taken to be x(0) = 0 and dt/dx(0) = 0. Plot the result in MATLAB. As part of your solution, do not use inbuilt Laplace and Inverse Laplace transform. computational functions. c) [10] Solve the governing equation (E1) using Laplace transforms to find the response of the system if r(t) = sin(10πt) . The initial conditions are taken to be x(0) = 0 and dt/dx(0) = 0 Plot the result in MATLAB. As part of your solution, do not use inbuilt Laplace and Inverse Laplace transform. computational functions. d) [5] Discuss the differences observed between the two responses in b) and c) and the main causes behind them. Question 2 [15 marks] A more accurate representation of the walking force in the lateral direction, r(t), has been derived empirically from studies of pedestrians. The experimental function found is depicted in Figure 4.A), while the form to which it can be approximated mathematically is shown in Figure 4.B). Its amplitude, G , for one person is 30 N, as listed in Table 1. The period of this force is determined by the frequency of people striding. The gait frequency (in other words, the frequency of walking) in the lateral direction is 1 Hz, which corresponds to a period of 1 second. Figure 4. A) Lateral component of the force r(t) acting on the bridge as a result from pedestrians walking found empirically. B) Function approximating the lateral walking force, r(t) as a square wave with amplitude 30 N and period equal to the lateralgait period, to be used in mathematical model.
Find the Fourier Series expansion of this periodic force function, r(t) . In your solution show the first four non-zero terms. Verify your result by plotting it in MATLAB.

Question 3 [20 marks] Up until now, we only considered the lateral displacement of a single point of the bridge, far from the support columns. Now let us study the vertical displacement of the entire platform between the supports. This is modelled by the wave equation (E2) where u(x, t) is the vertical displacement of the bridge, and x is now the horizontal position along the length of the bridge and t is time. Solve the wave equation assuming that

the constant a = 1,

the bridge has a length L: (0 ≤ x ≤ L),

the bridge is fixed at both ends u(0, t) = 0 (t ≥ 0), u(L, t) = 0 (t ≥ 0),

the bridge is initially at rest

the bridge is initially displaced to a general position f(x) u(x, 0) = f(x).

STAGE 2: Computational Model [35 marks] The following questions are asking you to set up a computational solution and perform a sensitivity analysis of the model. They resemble project-style questions and are less prescriptive. Question 4 [15 marks] Use numerical methods based on finite difference formulas to solve in MATLAB the problem described in Question 3, given by equation (E2). Use the same initial and boundary conditions but take f(x) = sin(πx) . That is, assume the bridge is

       fixed   at   both   ends, 
        initially   at   rest, 
          initially   displaced   to   a   position   f(x)   =   sin(πx). 
Use a time step Δt = 0.1 and a space step Δx = 0.25. Take a = 1 and L = 1. Show your results over a number of time steps and your annotated MATLAB code. Hint: You can represent the solution at time t−1 = (−Δt) as a function of the finite central difference approximation for the first derivative with respect to time at time t0 = 0. Question 5 [20 marks] Returning to the Ordinary Differential Equation model defined in equation (E1), use Laplace transforms to solve equation (E1), given the force r(t) is the function found in Question 2. The initial conditions are taken to bex = 0 and dt/dx(0) = 0. Support your solution with a graph, produced in MATLAB.
Perform. a sensitivity analysis and use its results to discuss the effect of the following different parameters on the lateral displacement of the bridge:

different number of people, N , walking on the bridge.
the magnitude of the damping coefficient, c , on the bridge displacement.
changes in the gait lateral frequency, f , to values within the range of 0.7 Hz to 1.2 Hz. Support your discussion with evidence of numerical results and simulations. Hint: As this is a linear system, the principle of superposition applies. The response of a system xss , when excited by an input function r(t) which is a series (a sum of multiple terms), is given by xss = xss1 + xss2 + xss3 + xss4 + ⋯ xssn, (E3) where xss1 is the system’s response to the firstterm of r(t), xss2 is the response to the second term, and similarly for each following term.

   加QQ codinghelp Email: cscholary@gmail.com
