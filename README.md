java cSCIE1000 Semester 2, 2024
Python and Communication Assignment
1 The scenario
A new public science museum in St Lucia is developing an exhibit. A feature of the museum is that
each exhibit item is accompanied by two explanations, each written for a different audience. One
explanation is pitched to the “science rookie” and the other to the “science enthusiast”. Patrons
read the explanation tailored to the level at which they feel most comfortable. Some characteristics
of typical patrons in each category are described in Table 1.
Table 1: Characteristics of different patrons
Patron Type Typical characteristics
Science Rookie Not familiar with scientiffc terminology or notation;
will need terminology explained using a simple vocabulary;
is unfamiliar with graphs;
may be a younger person, possibly 10+ years of age;
likes to press buttons.
Science Enthusiast Familiar with common scientiffc terminology and notation (not overly technical);
can handle terminology explained using somewhat sophisticated vocabulary;
is prepared to read longer passages of moderate complexity;
likes to know about modelling assumptions and limitations;
is familiar with graphs;
likes to press buttons.
The museum is planning an exhibition called “Plastics in our Oceans: A Cautionary Tale” which
examines how humankind’s voracious appetite for the production and consumption of plastic products
can have calamitous consequences for the natural environment around us. The aim of the exhibition
is summarised in the following passage from the exhibition prospectus:
Plastics have revolutionised the cost-effectiveness and versatility of manufacturing in the
post-war era. Plastics have become so commonplace in modern times that it is hard to
imagine life without them. However, as plastic consumption has increased, so too has
our knowledge and understanding of the potentially devastating impacts of mismanaged
plastic waste. As we plan for a more sustainable future, we must examine our dependency
on plastics and the consequences of inaction on the future health and prosperity of the
planet.
In this particular exhibit, patrons will gain a sense of scale for the rate at which the plastic products
humans produce are entering marine environments, both now, and in the future.
The museum director has asked the SCIE1000 teaching team for help in ffnding skilled volunteers
to develop exhibit items. Once developed, the items will be maintained and potentially modiffed by
museum staff, each of whom has a strong background in high-school mathematics combined with
a beginners level of Python experience. The director has been informed that SCIE1000 students
1are skilled at: making mathematical models using a mathematical toolkit familiar to any student
who has completed intermediate level high school maths (aka Mathematical Methods, or equivalent);
writing Python programs, including those which use arrays, loops, plots and user-defined functions;
and communicating scientific information to a variety of audiences.
2 An overview of the task
You will write an interactive Python program that will run on a machine in the exhibition hall at
the new science museum as part of this exhibition. Your program will guide users to a better understanding
of the scale of plastic production and the impact this may have on marine environments.
The information you need to create the relevant model is provided in Section 5 of this document,
and a high-level overview of how to complete the task is provided in Section 6.
This assignment requires you to produce two deliverables, (D1) and (D2), as outlined below:
(D1) A Python code file that satisfies the specifications in Section 7. This includes following the
logical flow laid out in the flowchart provided in Figure 3 (see Page 10).
(D2) An audio-video screencapture file (3-5 minutes long) in which you show your code and give an
overview of your approaches to modelling, programming and communication, aimed at museum
staff who will need to maintain your code. One way to create such a file is by recording with
Zoom (open a Zoom meeting, share your screen, and select Record → Record to this computer).
Please note that 5 minutes is a hard upper limit for the recording, and museum staff will stop
watching your video at the 5 minute mark.
3 Submission and grading
Both deliverables (D1) and (D2) are to be uploaded via the Blackboard submission link by 1pm on
October 15, 2024. If your video file is large, or if there are many other Blackboard users, it can take
time for your video file to load and you need to wait for your browser to complete the submission.
The UQ guidelines on Blackboard assignment submissions recommend submitting at least 3 hours before
the deadline, in case of any internet/computer/technical issues. If you do have technical issues,
you should contact the student IT service “AskUs” at the library. Late submissions without
an approved extension will be penalised according to the policy in the Course Profile;
consult the Course Profile for more information.
Your submitted code will be run and tested as part of this grading process. A rubric (grading criteria)
for this assignment is on Page 11. The file that you submit will be checked using software which is
specially designed to detect plagiarism in code. Consult the Course Profile for more information and
procedures concerning plagiarism.
This assignment has an advanced section which must be attempted by students aiming for grades of
6 or 7 (see the grading criteria for more explanation). The shaded section of the flowchart indicates
the requirements of this advanced section. If you have any questions, please contact the course
lecturers via the course discussion board (see Section 4 below).
24 About getting help
This assignment is a piece of summative assessment, designed to let you demonstrate your level of
mastery of several learning objectives in this course. As such, it is very important that the work you
submit is all your own. This does not mean that you cannot receive help in regards to this assignment,
but that help must be limited to general advice about modelling, Python and communication. This
task sheet has been carefully constructed, and part of your job is to interpret the information it
contains. Some choices have been left to your judgement, and this is intentional.
Remember that you must not look at anyone else’s code and you must not show your code to anyone.
Both of these actions are examples of behaviour that may be considered academic misconduct. No
code from your assignment attempt should be posted on the course discussion board, or any other
site, at any time. However, if you have problems with your code, you may develop some generic
sample code that demonstrates the issue that you are having (but does not relate to the assignment).
This can be discussed with others and/or posted to the course discussion board for assistance. All
such discussion board posts must be made visible to all students, so that everyone can see the question
and the answer from lecturers.
5 Modelling plastic entering the ocean
5.1 Plastic production
The term plastic refers to a broad group of synthetic polymers that have become ubiquitous in
modern manufacturing due to their low production cost and broad utility across a huge range of different
industries including packaging, consumer products, textiles, transportation, construction and
electronics. The origin of large scale plastic production dates back to the 1950s and global plastic
production has increased year-on-year in all but three years since then [1].
Figure 1: Examples of different modern plastic.
The museum exhibit aims to convey to patrons the scale of plastic production both now and into
the future, and what implications this may have for our oceans.
Selected data for the global rate of plastic production between 1975 and 2017 is provided in Table 2
[2].
3Table 2: Data for the annual global rate of plastic production from 1975–2017, sourced from [2] via
[3].
Year Rate of global plastic production (million tonnes·year−1
)
1975 46
1978 64
1981 72
1984 86
1987 104
1990 120
1993 137
1996 168
1999 202
2002 231
2005 263
2008 281
2011 325
2014 367
2017 420
Museum staff have provided a model for the rate of global plastic production, given by
P(t) = 50.4 + 2.606t + 0.143t
2
, (1)
Where P is the rate of global plastic production (in million tonnes·year−1
) and t is the time (in
years) since 1975. For modelling purposes, you may assume that any relationship for the global rate
of plastic production over the interval 1975–2017 can be extrapolated to future years. However, you
should clearly communicate to patrons when your model is being used to make predictions beyond
the time frame of the data provided.
5.2 Plastics entering the marine environment
The lifespan of a plastic product is the time that elapses between its creation until it becomes waste.
The lifespan of plastics varies significantly depending upon the type of plastic and how it is used. For
example, plastics used in building and construction typically have longer lifespans on the order of
decades, whereas plastics used in packaging may have an average lifespan on the order of months [4].
There are many different pathways for dealing with plastic wastes including reuse, recycling, thermal
destruction and disposal. However, reused and recycled plastics eventually need to be disposed of,
since these processes cannot be repeated indefinitely [1]. Mismanagement of plastic waste can lead
to plastics entering the marine environment.
Estimating how much plastic enters the world’s oceans is a complex problem. Jambeck et al. (2015)
developed a framework for estimating the amount of mismanaged plastic waste from coastal populations
that could potentially become marine debris. Based on data from 2010, they estimated that
approximately 2.96% of the plastic produced in that year ended up as ocean plastic [5], as depicted
4in Figure 2. Using this information, and the model for plastic production provided in equation (1),
you should develop a new model which estimates the global rate at which plastics enter the world’s
oceans. You may assume that this relationship between plastic produced and plastic entering the
oceans holds true in other years.
Figure 2: Infographic produced by [3] depicting the proportion of plastic produced that ended up in
the world’s oceans in 2010 based on [5].
5.3 A compounding problem
Once plastics have entered the marine environment they can remain there for a long time. In the
ocean, plastics do not generally biodegrade on a timescale that would contribute to the removal of
plastics from the environment. Instead, plastics at the sea surface are likely to undergo solar UVinduced
photodegradation reactions. This “weathering” of plastic materials in the ocean can cause
larger macroplastics to break down into microplastic debris [6]. The small size of such debris creates
additional problems for effective detection and can hamper efforts to remove plastics from the ocean.
Consequently, without targeted intervention, we can assume that all plastics that have entered the
ocean remain in the ocean.
5.4 Impact of plastic on marine environments
Ingestion or interaction with marine plastics (such as through entanglement, ghost fishing, dispersal
by rafting and habitat alteration) has been shown to affect more than 800 marine species, many of
5which are listed as being at risk according to the International Union for Conservation of Nature
[7, 8]. These effects can include ill health and death. Microplastics have been shown to collect in the
gut, digestive tract and gills of various marine species when ingested, and some species have been
shown to accumulate microplastics in other tissues through translocation [8].
As microplastics contaminate the environment, their presence has been demonstrated
in the food chain. At lower trophic levels in the marine environment, the presence of
microplastics has been reported in zooplankton, chaetognatha, ichtyoplankton, copepods,
and salps. Microplastic contamination also occurs at higher trophic levels, in invertebrates
(polychaetes, crustaceans, echinoderms, bivalves) and vertebrates (fish, seabirds,
and mammals). Plastic particles reach them either through direct consumption or through
trophic transfer.[10]
5.5 Looking to the future
Geyer (2020) suggests that, based on current trends in plastic production, waste generation, and
waste mana代 写SCIE1000、Python
代做程序编程语言gement, recycling and incineration will not be sufficient to sustainably manage plastic
in the long term. Hence it will be important to consider mechanisms for reducing the amount of
plastic produced and consumed [1]. Furthermore, sustainable consumption and production have been
identified by the United Nations as a key sustainable development goal as part of a larger collective
of 17 goals aimed at providing a global vision for achieving a sustainable, just, and safe planet [9].
6 A detailed overview of the task
Your assignment submission must follow the specifications listed in Section 7. Below, we first give a
high-level overview of how to approach the main section and the advanced section of this assessment
task.
To complete the main section, you will need to:
 Determine an appropriate mathematical function to model the global rate at which plastics
enter the marine environment using the information provided in Sections 5.1 and 5.2, and
clearly communicate the potential scale of this issue to patrons. Your model will be based on
the one provided by museum staff in equation (1). You will write a function in your code which
implements the ocean plastics model. Your function should take one input, time in years since
1975, and return an estimate of the global rate at which plastics enter the marine environment
(in million tonnes· year−1
) at that time.
 Produce a graph of the model of the rate of plastic entering the ocean.
 To give patrons a sense of the scale of plastic entering the ocean, you should include a comparison
for patrons which depends on the output of your model for the global rate of plastic
entering the ocean. Your comparison should provide patrons with a clear understanding of the
scale of the mass of plastic entering the ocean in their chosen year, by comparing it the mass
of an object or objects that would be familiar to the patrons.
6 Communicate appropriately with museum patrons as informed by the main section of the
flowchart in Figure 3.
 Include a description of how you approached this section of your code in your screen capture
video (D2), including (briefly) how you developed your models and the overall code structure.
To complete the advanced section, you will need to:
 Explore other models for the rate of plastics entering the ocean, using methods covered in
SCIE1000. You will write a function in your code which implements your chosen alternative
model. Create a graph that compares your alternative model to the quadratic model and
present this to the science enthusiast.
 Calculate the predicted doubling time from the present year using your alternative model.
 Communicate appropriately with museum patrons as informed by the the advanced section of
the flowchart in Figure 3.
 Include a description of how you approached this section of your code in your screencapture
video (D2), including how you developed your models.
7 Specifications for your submitted file
7.1 Specifications about the Python
 Museum staff have supplied a flowchart describing how the program should run (Figure 3 on
Page 10). Your code must be an implementation of the flowchart provided.
 Your code must be well-structured and follow the guidelines for programming practice, as
introduced in SCIE1000.
 Whenever you prompt the user for information, you may assume they enter a suitable number,
and you can store their answer as an integer or as a floating point number as appropriate. You
do not need to check for incorrect inputs.
 You may only use Python commands introduced in SCIE1000. Recall that museum staff
must be able to maintain and modify the code, so you may only use commands that they
understand. Museum staff have a beginner’s level of experience using Python, which you may
regard as the equivalent of a student who has taken SCIE1000. The Python commands you
have covered in this course should be more than sufficient to complete the assignment.
 Museum staff have identified functions that they think will be useful in possible modifications
and extensions of the code. You must define these functions in your code. You should
use these functions in your code as appropriate. You may define other new functions as needed.
77.2 Specifications about the communication
 All messages to the user, including prompts to enter data, should communicate in a manner
appropriate for the level of patron and should serve the purpose of the program.
 You should write no more than a couple of sentences for each piece of information you explain
to the user. Follow the principles for communication in science as described in Appendix B of
the workbook. Be precise, clear and concise!
 You should use units appropriately in your communication with the user. Make sure you are
aware of the units of values being passed into functions and the units of values being returned
from functions.
 You should include useful and appropriate comments in your code to help the museum
staff who may need to maintain and modify the code. Any variable names and function names
you define should be chosen with communication in mind.
 Whenever you produce a graph you should provide appropriate labels and accompanying
explanatory text.
 Your screen capture video should provide a clear overview of how your code works
and why you made the choices you did. This does not replace excellent commenting in
the code.
 To reference sources other than those cited in this task sheet, you should include a bibliography
as comments at the end of your code, to show the museum staff maintaining the code where
you obtained any relevant information you used. You may use any referencing style.
7.3 File type and file name
 Your assignment (D1) should be saved as a .py file called PlasticOceans********.py with
the string ******** replaced by your student number.
 Your screencapture audio/video file (D2) should be saved as Explanation********.mp4
with the string ******** replaced by your student number.
 It is your responsibility to ensure that the file types are correct.
8References
[1] Geyer, R. (2020). A brief history of plastics. In: M. Streit-Bianchi et al. (eds.), Mare Plasticum – The Plastic
Sea.
[2] Geyer, R., Jambeck, J.R. and Law, K.L. (2017). Production, use, and fate of all plastics ever made. Science
Advances: 3:e1700782 DOI:10.1126/sciadv.1700782
[3] Ritchie, H., Samborska, V. and Roser, M. (2023). Plastic Pollution. Our World in Data: https://
ourworldindata.org/plastic-pollution
[4] Wang, C., Liu, Y., Chen, W.-Q., Zhu, B., Qu, S., Xu, M. (2021). Critical review of global plastics stock and flow
data. Journal of Industrial Ecology. 25: p. 1300– 1317. https://doi.org/10.1111/jiec.13125
[5] Jambeck, J.R., Geyer, R., Wilcox, C., Siegler, T.R., Perryman, M., Andrady, A., Narayan R. and Law, K.L.
(2015). Plastic waste inputs from land into the ocean. Science: 347(6223), pp. 768-771. DOI:10.1126/science.
1260352
[6] Andrady, A. L. (2015). Persistence of plastic litter in the oceans. In Marine anthropogenic litter (pp. 57-72).
Springer, Cham.
[7] Marine Debris: Understanding, Preventing and Mitigating the Significant Adverse Impacts on Marine and Coastal
Biodiversity. Technical Series No.83. Secretariat of the Convention on Biological Diversity, Montreal, 78 pages.
[8] Steer, M., and Thompson, R. C. (2020). Plastics and Microplastics: Impacts in the Marine Environment. In Mare
Plasticum-The Plastic Sea (pp. 49-72). Springer, Cham.
[9] United Nations Department of Economic and Social Affairs Sustainable Development. (n.d.) Ensure sustainable
consumption and production patterns. https://sdgs.un.org/goals/goal12. Date accessed: 26th April, 2022.
[10] Hollman, Peter CH and Bouwmeester, Hans and Peters, Rudolphus Johannes Bernhardus (2013). Microplastics
in aquatic food chain: sources, measurement, occurrence and potential health risks. In RIKILT.
9Print a welcome message appropriate for all patrons. 
Print a statement explaining the patron types and prompt the user to enter their patron 
type. 
Print an introduction about plastics and this exhibit appropriate for the chosen patron 
type. 
Print a statement about the scale of plastic production and plastics entering the ocean and 
how this has changed over time as appropriate for the chosen patron type. 
Enthusiast?
Display a graph of the model of the rate of plastic entering 
the ocean vs. years since 1975 over the period 1975—2050. 
Your graph should display estimated data points by year 
given in Section 5.1. Your model should use a solid line 
when interpolating and a dashed line when extrapolating. 
Prompt the user to enter a year between 1975 and 2050.
Yes
No
Calculate the estimated rate of plastic entering the ocean in that year using your 
model and report a message with a useful comparison, as appropriate for the 
chosen patron type.
 
Ask the user if they wish to choose another year. 
Print a statement appropriate for the patron type explaining why plastics accumulating in 
the ocean over time is an issue.
Explain at least two limitations of the quadratic model that has been used.
No
Yes
Enthusiast? Graph your new model with the quadratic model and 
compare the two.
Print an appropriate farewell message. 
Advanced
No
Yes
 Ask the patron to estimate how long it will take for the rate 
of plastic entering the ocean to double from the current level, 
using your new model. 
Inform the patron of the predicted doubling time.
Figure 3: Flowchart for the interactive program (shaded section indicates the advanced section).
10Python and Communication Assignment Grading Criteria
Your marks for the Python and Communication sections of the assignment (each on a 1–7 scale)
are calculated by combining the mark that best matches your answers for the main section with the
marks for the advanced section. Your overall mark will thus be up to a maximum of 14. The table
below shows the criteria for each grade.
Mark Python (1–7) Communication (1–7)
1 The code is limited and displays little understanding
of the modelling involved.
Communication is very poor and would be
difficult to understand for any audience.
2 The code fails to run for any input, does
not meet the specifications, and/or has serious
conceptual errors in the modelling.
 The communication of the relevant scientific
information (in the code and to patrons)
is generally poor.
3 The code runs for some expected inputs,
meets at least some of the specifications,
and/or may have some significant conceptual
errors in the modelling.
The communication of the relevant scientific
information (in the code and to patrons)
lacks clarity or is not at the appropriate
level for each target audience.
4 The code runs without error for most
inputs, mostly meets the specifications,
and mostly represents the mathematical
modelling with perhaps some conceptual
and/or mathematical errors.
The communication of the relevant scientific
information (in the code, the screencapture
video, and to patrons) is adequate
for each target audience. There may
be some limitations in the communication
within the code and/or to patrons.
5 The code runs without error for all expected
inputs, largely meets all the specifications,
and accurately represents the
modelling with perhaps only one or two
minor errors.
The communication of the relevant scientific
information (within the code, the
screencapture video, and to patrons) is
mostly clear, fluent, appropriately concise,
and uses a level and style appropriate for
each target audience.
Advanced Section
0 Not attempted, or the advanced code has
significant conceptual errors.
Not attempted, or the communication in
the advanced section is poor.
+1 The code for the advanced section runs
with only minor errors and mostly represents
the task with some conceptual or calculation
errors.
The level of communication is adequate
throughout the advanced section but
would require some editing before use in
an exhibit. The advanced section is communicated
in the screencapture video.
+2 The code for the advanced section runs
without error and accurately represents
the task with at most one minor error.
The level of communication is clear
throughout the advanced section and
would be suitable for use in an exhibit
with perhaps only one or two small
changes. The advanced section is clearly
communicated in the screencapture video.
11

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
