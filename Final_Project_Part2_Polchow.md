# Project Design Writeup and Approval Template

Follow this as a guide to completing the project design writeup. The questions for each section are merely there to suggest what the baseline should cover; be sure to use detail as it will make the project much easier to approach as the class moves on.

### Project Problem and Hypothesis
* What's the project about? What problem are you solving?
The project is to determine what the key factors are related to Middle School Student's performance on the CCLS (Common Core Learning Standard) state exam for Mathematics. The score a student makes is a determinant in whether or not the student can pass on to the next grade, and it also affects the rating schools receive. The main question I want to solve is "Can effective teachers truly make a difference on a city-wide basis or are students' performance predetermined by their racial and socioeconomic background?"

* Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?

Students have a score ranging from 1-4, and they are diagnosed as Level 1 (Well Below Proficient), 2 (Partially Proficient), 3(Proficient), or 4 (Exceeding Proficient) depending on where they lie on that spectrum. Students are considered to have met grade level standards if they receive a score of 3 or above and not at grade level if they receive a score below.
Due to this manner of scoring I could either analyze the score as a continuous variable (number 3 digit number between 1 and 4) or as a categorical variable (pass and fail) depending on what type of analysis I end up performing.

* What kind of impact do you think it could have?

With this information, school districts could better allocate resources to the areas that have the largest impact on whether or not a student is successful on the exams. The results could be analyzed and the findings could perhaps be extrapolated to other urban areas around the country.

* What do you think will have the most impact in predicting the value you are interested in solving for?
I predict that the most important factors will be income level, race, and teacher effectiveness.

### Datasets
* Description of data set available, at the field level (see table)
The data is held in 2 csv documents. 
Here are all the variables that I have in addition to the dependent variable (score on CCLS exam)
1)Quality Report Ratings
-Rigorous Instruction
-Collaborative Teachers Rating
-Supportive Environment
-Effective Leadership
-Strong Family-Community Ties
-Trust Rating
-Student Achievement Rating

2)Demographics
-Race
-Income Level
-English Language Learners
-Students with Disabilities
-Percent in Temporary Housing
-Gender

3)Other
-Percent of teachers with above 3 years experience
-Years principal has been at school
-Student/Teacher attendance rate
-School safety
-Size of school
-District
-Borrough

The data sets are complete, and I do not see any "NaN"s upon first inspection.

### Domain knowledge
* What experience do you already have around this area?

I'm a second year teacher, and I've had my own anecdotal observations about what makes students successful vs unsuccessful. I've also heard countless opinions from other teachers about how or why students score the way they do on the state exam.

* Does it relate or help inform the project in any way?

Yes.

* What other research efforts exist?

New Jersey performed research entitled "Predicting Middle Level State Standardized Test Results Using Family and Community Demographic Data." They used "simultaneous multiple regression" and "hierarchical linear regression" to develop their model.

National Center for Educational Statistics performed a school level analysis to determine student success based off of different factors. (https://nces.ed.gov/pubs2000/2000303.pdf) Their method was linear regression.

 

### Project Concerns
* What questions do you have about your project? What are you not sure you quite yet understand? (The more honest you are about this, the easier your instructors can help).
1) I'm not sure which variables I should attempt to use as predictors. I have quite a few.

2) I'm not sure if I should treat this as a regression or as a classification problem of either "pass" or "does not pass" based off of certain characteristics.


* What are the assumptions and caveats to the problem?
    * What data do you not have access to but wish you had?
    Amount of time spent watching TV/using phones. Crime staistic for each neighborhood.
    * What is already implied about the observations in your data set? For example, if your primary data set is twitter data, it may not be representative of the whole sample (say, predicting who would win an election)
    
    It's implied that this information is only pertaining to students in NYC DOE schools. It does not include private or charter schools.
    
* What are the risks to the project?
A risk is that there will be a high multicollinearity between a lot of these variables which will decrease the effectiveness of the model.

* What's the cost of your model being wrong? (What's the benefit of your model being right?)

No real costs unless decisions are made based off the data.

* Is any of the data incorrect? Could it be incorrect?

The chance of the data being incorrect seems to be very slim. The quality survey results, however can be subjective and vary depending on the relationship the Principal has with the DOE.

### Outcomes
* What do you expect the output to look like?
I expect two different possible outputs. 
Option 1: A linear regression that includes each variable. (if I decide to go down the route of keeping the scores as continuous variables)
Option 2: A decision tree/random forest that breaks down each variable to determine the likelihood of passing given certain characteristics

* What does your target audience expect the output to look like?
Nobody knows about this project except for me.

* What gain do you expect from your most important feature on its own?
I expect to gain a better understanding of what leads to successful education. Is it truly possible to overcome large scale.

* How complicated does your model have to be?
As complicated as necessary in order to get some results that make sense and are presentable. The simpler the better.

* How successful does your project have to be in order to be considered a "success"?
After this part-time program, I want to apply to be a part of a full-time data science bootcamp. I want my model to be complex and insightful enough to impress any admissions committee when I apply to their program.

* What will you do if the project is a bust (this happens! but it shouldn't here)?
If this project is a bust, life will go on. But I won't let it bust!
