# Lotka-Volterra Competition Modeling
Modeling the changing landscape of IT Work culture
Introduction :
Before the pandemic, there was only a small group of workers who worked remotely full time, and a much larger class of workers who telecommuted occasionally or simply sometimes took work home. With the outbreak of COVID, quarantine and lockdown has permanently affected work environments. As we look towards a post-covid future, it is desirable to understand and predict how remote and in-person work will evolve over time. As the pandemic has shown, many IT jobs can be performed remotely. However, some jobs will always require in person roles (ex. service industry or classified systems). In the future, is it possible that all employees will be able to work remotely? In this report, competition model will be used to simulate the change of in-person and remote work overtime, perform analysis to find potential equilibria and predict the future of remote work in the IT industry.

2.1 Assumptions:

Following assumptions were made to simplify the mathematical model:

Carrying Capacity: There is a maximum number of employees who can work remotely or in person. This implies the overall size of the IT labor market is fixed.
Logistic Growth: In the absence of competition from the other form of work, the number of people working remote/in-person work will grow logistically towards their carrying capacity.
Two Worker Classes: Jobs/Workers are classified as either primarily remote or primarily in person. 
Flow of workers: The rate of change of workers entering, exiting (i.e retiring), and switching from in-person to remote jobs are constant.
Industry: This model focuses only on jobs in IT industry

2.2 Compartmental model :

There are two separate quantities that vary with time: the number of employees work remotely and the number of employees work in person. Therefore, two equations were developed, one for the rate of change of remote workers and one for the rate of change of in-person workers. The only input for each pool is workforces entering the IT field, like new graduate students, people who change career path etc., and the only output is employees leaving the industry, such as people who are retired or quit. However, workers can choose if they want to work remotely or on site. This is illustrated in the input-output compartmental diagram below.  
Here in the model, the natural workforce flow gained or lost are distinguished with the rate of change of workers switching between working environments.
 
2.3 Equation and constants :

For the rate of change of employees entering and leaving IT industry, it is denoted as {r1N1} and {r2N2}. The carrying capacities are denoted as k1 and k2. Once the numbers of employees go above the carrying capacities k1 and k2, they will decrease back to k1 and k2. For workers change from work from home to in person, it is denoted as {c12N2N1}, since it is proportional to the number of in-person workers. Similar for workers switch from in person to work remotely.


N1: Number of remote workers
N2: Number of in-person workers
r1: Self-regulation term of remote workers (number of workers entering the IT field
remotely minus the number of workers exiting the IT field remotely)
r2: Self-regulation term of in-person workers (number of workers entering the IT field
in-person minus the number of workers exiting the IT field in-person)
k1: Carrying capacity. Maximum number of remote workers
k2: Carrying capacity. Maximum number of in-person workers
c12: Competition factor for remote workers (workers switching from remote to in-
person work)
c21: Competition factor for in-person workers (workers switching from in-person to remote work)

2.4 Equilibrium Levels :

To get results for equilibrium points, we let dN1dt=0 and dN2dt = 0. This gives (0,0), (0,k1), (k2,0) and (r₁r2k2-c₁₂r₂⁄r₁r2k₁k2-c₁₂c₂₁ ,r₁r2k1-c₂₁r₁⁄r₁r2k₁k2-c₁₂c₂₁ ), we get this when we find intersection of lines N1=k₁(1-C₁₂N2r1) and N2=-k2c21r2N1+k2. There are 9 unique cases to analyze with the 2 lines representing N1=k₁(1-C₁₂N2r1) , N2=-k2c21r2N1+k2. Later in the graphical analysis, WFH and WIO will be used to represent remote workers and in-office workers

2.5: Estimation of Parameters:

Based on the Bureau of Labor Statistics, data shows that 71% to 77% of people in the Information Technology field have the ability to work remotely. Therefore, k1 is set to be k1 = .75*k2, to represent that all jobs could be done in the office, but only 75% could be done remotely. 
r1, r2, c12, and c21 were chosen using the bounds from graphical analysis. 
r1 should b e larger than r2 as remote jobs grows faster than in-office jobs 
c21 should be larger than c12 as more workers switch from work in office to work from home
k1: 30000
k2: 40000
r1: 0.7
r2: 0.4
c12: 5.133 x 10^-6
c21: 1.2 x 10^-5

2.6 Interpretation :

Over time, the model shows remote work growing as much as it can and approaches its carrying capacity. It means that when employees have the option to choose between work from home and work in the office, work from home wins. But there will always be some level of in-person work, since not all IT jobs have the ability to be fully remote (research suggests about 25% cannot be remote). The model also illustrates the rapid change we have seen from in-person to remote dominated work, since the pandemic showed that remote work is possible, productive, and more desired for many people.

2.7  Model Limitation :

In the real world, the job market size changes - there is not a set carrying capacity
Rather than remote vs in-person, the reality is much more complex. More people are in the office some days, and working from home other days. There is not such a harsh line between the two groups of workers anymore.
Constants are not constant in real life: hiring rates, retirement rates, and rate of moving between types of work is dependent on many factors, such as:
Current mass retirements from baby-boomer generation reaching retirement age
Lower hiring and less retirements during a recession
Technological advances modifying the size and growth of IT field
How desirable the IT field is compared to other jobs

3.0 Conclusion :

Based on our graphical and computational analysis, it can be concluded that most jobs in the IT industry in the future will be shifted to working from home with minimum workers going to office to maintain functionality. However, this is a simplified model, the real world data will have more decision factors and complex features. More real-world data will be needed to mimic this situation.  



