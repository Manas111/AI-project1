





     Learning Outcomes: (As we have seen with GPS, customers are ready to accept #AI, but only if it provides real value and improves their brand experience.)


Declaration:

I declare that this Assignment is our team work. We have not copied it from any other students work or from any other source except where due acknowledgement is made explicitly in the text, nor has any part been written for me by any other person.


Evaluator’s comments (For Instructor’s use only)




General Observations                    Suggestions for Improvement       Best part of assignment

 












	



Evaluator’s Signature and Date:







Marks Obtained:  	                                             Max. Marks:_________________







Abstract
Simple navigator/GPS navigation systems use stored map information for determining optimal route selection based on a shortest path algorithm. This technique is quite successful in getting you to where you want to go in a reasonable time and is fault tolerant in the sense that it can automatically reroute in case of error. One disadvantage of this approach is that it does not have any memory. It does not automatically remember the actual time it took you to get there nor does it learn from that experience and use the actual measurements to improve future route selection.  A simple method for modifying a GPS navigational system to incorporate a simple learning paradigm using velocity profiles is described. In addition to learning, these velocity profiles can also be used to extract features from the environment which can then be used to further improve the accuracy of optimal route selection. It is assumed to be completely autonomous which means that it requires no user input or intervention. All of the required information is derived from recording GPS location, date and time. 
INTRODUCTION  
How many times have you wondered which of two routes were better and decided to go one way one day and the other way the next day and then compare the mileage or the time? That way you would know once and for all which was better and always go that way. However, it is generally inconvenient to try to measure time or distance and inevitably we forget to do so. In any event the learning experience is not perfect.
    Fortunately, it would be easy for a GPS Navigational System (GNS) to automatically perform this task for you. The idea is to emulate how a human being might use prior experience to determine an optimal route given that the person had a perfect memory of every trip they had ever made and the time it took them to traverse each route segment as well as the time and date. The person starts out with zero knowledge, as if they had just moved to the area for the first time. As more and more data are collected from day to day driving experience the better the system becomes in selecting optimal routes and accurately estimating the time from starting point to destination.  The system adapts to both the traffic environment and the habits of the driver.
When planning a route from starting point to destination, a typical person considers the time of day, the day of week and any seasonal considerations.  A classic example would be a cab driver. A good cab driver might take a different route to the airport depending on the time of day. A GNS system can make use of this same technique by having a perfect memory of every trip ever taken. As time goes on and more trips are taken and the ability to choose the best route will improve over time. Of course, it would require extra processing and data storage to perform this function. However, CPU processing power has been steadily increasing while the price of mass storage devices has been dropping precipitously. In the last few years the price of mass storage devices has been dropping by a factor of two every six months to a year. As a result, large amounts of data can be stored inexpensively, and this is no longer the limiting factor it might have been in the past. The use of measured data to improve GNS performance has been studied previously. For example, the approach taken in aggregates data collected from many different individuals. This can shorten the learning curve initially as you gain from the experience of other people. However, the disadvantage is that it is not tailored to your particular driving habits which is an important factor in obtaining accurate results.   
Figure 1 shows a typical example similar to what the average person might face on any given day. Suppose that you must drive to work every Monday through Friday morning during rush hour traffic. However, to get to work you have to get to the highway first, so the problem is how to get from point A to point B. From the map is there are many alternative routes.  One of these routes starts at the intersection at point A and follows Loiza (route 37) and at the intersection goes left onto José de Diego.  According to MapQuest that is a distance of .33 miles and will take one minute (an average speed of 20 mph). On a Saturday morning at 8 am there is very little traffic, and this would be reasonably accurate. However, at 3pm on a weekday this could easily take 20 minutes or even half an hour under extreme conditions. In practical reality the best way to go is often not static and often depends on the time of day and the day of the week.  An alternative route shown follows Calle San Jorge to Colon to Parque to Lopez Landron.

FIG :- 1  Two Possible Route Alternatives

During congested periods it has been determined by experience that this zigzag alternate route is significantly faster (perhaps taking 5 minutes instead of 20).  Although this might be an extreme example, it shows that routing decisions based purely on distance can lead to large errors in the result. In some cases, it doesn’t make much difference which way you go. However, there may be times when it is makes a big difference. For example, you are going to the airport and you are running a bit late. Or what if it involves the use of an emergency vehicle where time is of the essence and you have to play the odds.

LITERATURE REVIEW

Factors that Affect the GPS Accuracy 
     Initially, in order to identify the factors that affect the accuracy of a GPS signal, we conducted an initial survey with a group of volunteers. The survey was initiated in order to identify the top issues that is faced by users of GPS applications. We managed to obtain 50 respondents that had varying levels of experience with such applications. From the results, 92% of the respondents have used a GPS based applications before. Out of the 92% of respondents, 78.3% has faced inaccuracy of GPS when using the GPS based application. Besides that, 78.3% of the respondents agree that the inaccuracy of GPS is mainly caused by a weak GPS satellite signal. In addition, some of the respondents also agreed that the GPS receiver errors and environment factors plays a role in the increased inaccuracies of GPS. Based on the results we obtained from our survey, we identified related works about the factors that affect the accuracy of GPS from the existing research as shown in this section. 
 
According to the related work found from the existing research, both the GPS receiver and the satellite signal transmission can affect the accuracy of GPS positioning.  The accuracy of GPS depends on the signal strength of satellite signals and the receiving process of the receiver  . Before the year 2000, the most important factor in degradation of GPS signal error is caused by selective availability (SA)   as selective availability can cause less accurate positioning. The feature is permanently deactivated due to the broad distribution and worldwide use of the GPS system  . At the moment, there are different factors that can affect the accuracy of GPS. Table 1 highlights some of the major effects and errors rates that could occur with the GPS technology. 
 

Table 1.  Factors related to error rates. 
 

                  
From Table 1, it can be seen that ionospheric effect causes the most significant error in GPS accuracy. In the ionosphere at the height of 80 – 400 km a large number of electrons and positive charged ions are formed by the ionizing force of the sun. These layers refract the electromagnetic waves from the satellites which leads to an elongated runtime of the signals. Figure 1 shows the region of ionosphere and troposphere 
 
 
Figure 1.  Ionosphere and Troposphere Regions  
 
To sum up, the main factor that leads to GPS signal error can be classified into 3 aspects, namely GPS satellite signal, GPS receiver and usage environment as shown in Table 2 below. 
 
Table 2.  General factors that affect the accuracy of GPS positioning [2, 3]. 
 

 
2.2. Main Methods to Improve GPS Accuracy 
 
There are a number of existing methods to improve the accuracy of GPS. Table 3 highlights the most common methods implemented today. 
 
Table 3.  Methods to improve accuracy of GPS positioning 
 

 
3. ANALYSIS 
 
In this section, the results about which existing improving methods can minimize the factors that affect the GPS accuracy are tabulated and analysed. These results are obtained from the research papers that we identified. 
 
3.1. Reference Station Networks 
 
Reference Station Networks was used by Wübbena to improve the accuracy of GPS  . According to Wübbena  , the factors that can be reduced by utilizing this method are shown in the table below (Table 4). 
 
Table 4.  Factors that can be improved via the Reference Station Networks method   
 

 
Based on Table 4, the usage of Reference Station Networks can minimize ionosphere and troposphere delays as well as orbital errors. By minimizing these factors, the accuracy of GPS can be improved. 
 
 
3.2. Kalman Filter Algorithm 
 
The Kalman Filter Algorithm was used by Qi   and Malleswari   to minimize some of the factors that affect the accuracy of GPS. Table 5 shows the common factors that affect the accuracy of GPS which can be minimized by this algorithm. 
 
Table 5.  Factors that can be improved via the Kalman Filter Algorithm method [7,8] 
 

 
 
According to the table above, Kalman Filter Algorithm can minimize four factors that affect the accuracy of GPS, which are Satallite Clock Errors, Receiver Clock Errors, Ionosphere and Troposphere Delay and Multi-Path Distortion. By minimizing these four factors, the accuracy of GPS can be improved. 
 
3.3. Map-Matching Algorithm 
 
The Map-Matching Algorithm was used by Alain in  . This algorithm was used by Alain to improve the accuracy of user’s location in a GPS based system. According to Alain  , this algorithm is applied to the GPS based system so that the user’s location which is not accurate can be reconciled with a map/network which is not accurate as well. Hence, the factors that affect the GPS accuracy cannot be minimized by using the algorithm as shown in Table 6. 
 
 
 
 
 
 
 
 
 
 
 
 
Table 6.  Factors that can be improved via the Map-Matching Algorithm method   
 

 
3.4. Perceptive GPS 
 
Perceptive GPS (PGPS) was used by Chung   is to improve GPS accuracy. According to Newton’s Third Laws, This algorithm uses GPS data as navigation reference units to infer the motion of the carrier. The PGPS method does not require an auxiliary hardware to support it and it is also sensitive to the carrier’s behaviour. The table below (Table 7) show the factors that affect the GPS positioning accuracy and the specific factors that cannot be mitigated by the method. 
Table 7.  Factors that can be improved via the Perceptive GPS   
 

 
 
According to the Chung  , this algorithm can minimize only three factors that affect the accuracy of GPS, which are Receiver Clock Errors, Number of Satellite visible, and Satellite Position which have been shown in the table above. Hence, the accuracy of GPS can be improved by minimizing these three factors. 
 
3.5. Google Map GPS Tracking Enhancement 
 
Lin used an algorithm to improve the accuracy of GPS tracking in the Google Map application  . This algorithm does not specifically minimize any factors that affect the accuracy of GPS but it improves the design for a location displayed on the map’s application  . Table 8 highlights the effectiveness of the GPS Tracking Enhancement in terms of mitigating specific inaccuracy factors. 
 
Table 8.  Factors that can be improved via the Google Map GPS Tracking Enhancement method   
 



Proposed methodology 
  
A. Integrated System Scheme
The INS/GPS integrated navigation system adopts loosely-coupled combination mode, and the fusion method incorporating data preprocessing algorithm and LSTM is proposed in the system, as shown in Figure 1.


FIGURE 1.
Proposed system structures. (a) Training mode. (b) Prediction mode.
When GPS signals are available, the system operates in training mode, as shown in Figure 1(a). The position PI , velocity VI and attitude AI offered by INS and position PG provided by GPS are integrated into KF. The estimated position error δP , attitude error δA and velocity error δV are used to correct the navigation results of INS. The data preprocessing algorithm based on EMDTF is used to eliminate the noise in IMU data. Meanwhile, the LSTM module is trained, whose inputs are the current angular rate wbib and specific force fbib , while the output is GPS position increment ΔPG .
Once GPS signals are unavailable, the system works in prediction mode, as shown in Figure 1(b). The current angular rate wbib and specific force fbib are provided as inputs to LSTM, and the output of LSTM is the predicted GPS position increment ΔPG . The predicted value ΔPG can be accumulated with initial position information PG0 to get pseudo-GPS position PpseG , which is then used to limit the divergence of inertial navigation error.
B. Data Preprocessing Algorithm
The data preprocessing algorithm combines the advantages of empirical mode decomposition (EMD) and wavelet threshold filtering, which can eliminate noise from IMU signal and retain useful signal as much as possible. First, the EMD adaptively decomposes the noisy IMU signal into a series of intrinsic mode functions (IMFs) according to amplitude and frequency. It overcomes the shortcomings of the fixed base function of wavelet transform and has a strong local adaptive. Then, the wavelet threshold filtering is applied to high-frequency IMFs, which separates the useful information in the high-frequency IMFs. How to select the threshold value and threshold function is the key to the wavelet threshold filtering. By comparing the effect of different methods to deal with IMU signal, heuristic threshold and soft threshold function are applied in this paper. Finally, these IMFs are added with IMFs of low frequency and residual signal to achieve de-noising signal. Figure 2 is the flowchart of IMU signal de-noising algorithm.


FIGURE 2.
The flowchart of IMU signal de-noising.
 
C. Long Short-Term Memory Neural Network
The traditional neural networks cannot adaptively use the previous data. To achieve information persistence, the LSTM neural network is used in this paper. The LSTM is a special type of recurrent neural network (RNN), and has been wildly used in many fields (e.g. financial market prediction [32], wind speed forecasting [33], sentiment classification [34], voice detection [35]). Considering the advantages of LSTM, the LSTM is firstly proposed to forecast pseudo GPS position when GPS signals are unavailable, which establishes the relationship between the outputs of IMU and the GPS position increments. The inputs of LSTM are six parameters, while the inputs of traditional ANN (i.e. the model in reference [21]) are eighteen parameters.
The memory cell is the core component, and it consists of input gate (i.e., it determines if the input data will be used), forget gate (i.e., it decides if the last state will be forgotten) and output gate (i.e., it calculates if the information will be propagated). Figure 3 shows the structure of LSTM network.


FIGURE 3.
The structure of LSTM neural network.
 
The forward pass equations of LSTM are given by:
⎛⎝⎜⎜⎜ftitotgt⎞⎠⎟⎟⎟=ct=ht=⎛⎝⎜⎜⎜σσσtanh⎞⎠⎟⎟⎟W(ht−1xt)=ft⊙ct−1+it⊙gtot⊙tanh(ct)(11)(12)(13)
View Sourcewhere xt denotes the input data at time step t , ht denotes the hidden (output) state; functions σ and tanh are applied element-wise; it denotes input gate, ft represents forget gate, ot means output gate, and gt is used to modify the cell state ct ; W is corresponding weights matrix; ⊙ represents the Hadamard product.
The above LSTM can forecast pseudo GPS position when GPS signals are unavailable. The prediction procedures are as follows.
Firstly, the LSTM neural network is trained. The inputs are the current angular rate wbib and specific force fbib , and the output is GPS position increment ΔPG . Secondly, the trained LSTM neural network is used to predict ΔPG . The inputs are the same as the first procedure. Lastly, the predicted value ΔPG is accumulated with initial position information PG0 to get pseudo-GPS position PpseG .
SECTION IV.
Performance Evaluation
A. Numerical Simulations
To verify the proposed methodology, numerical simulations are performed. The specifications of sensors are shown in Table 1. The vehicle movements are various, and its detailed motion states are shown in Table 2.
TABLE 1 Sensors’ Specifications


TABLE 2 Motion States of the Vehicle


To validate the data preprocessing algorithm proposed in section III comparative simulations of de-noising algorithm or not are carried out under the mode that GPS signals are available. During this simulation, EMD decomposes the IMUs signals. Then, the high-frequency IMF1 and IMF2 are preprocessed by wavelet threshold filtering. Finally, these IMFs are added with IMFs of low frequency and residual signal to achieve de-noising signals. Since the vehicle is assumed to move only in the horizontal plane, the errors of directions of east and north are shown in the paper. Figure 4 and Figure 5 depict the velocity and position errors, respectively. Table 3 evaluates the de-noising algorithm.
TABLE 3 Evaluation of De-Noising Algorithm




FIGURE 4.
The velocity errors of de-noising algorithm. (a) East velocity error. (b) North velocity error.
 


FIGURE 5.
The position errors of de-noising algorithm. (a) Longitude error. (b) Latitude error.
 
From Figures 4 and 5, it is obvious found that by using the data preprocessing algorithm, the accuracy of velocity and position have been significantly improved. As shown in Table 3, the max errors of the original algorithm for east velocity, north velocity, longitude and latitude are 0.2161m/s, 0.2288 m/s, 1.8825 m and 1.8824 m, respectively. After processing by the de-noising algorithm EMDTF, the max errors of the corresponding components are reduced to 0.0837 m/s, 0.1313 m/s, 0.9939 m and 1.0684 m, respectively. The improvement rates are about 61.28%, 42.61%, 47.2% and 43.24%, respectively. The corresponding root mean square error (RMSE) values are reduced by about 9.12%, 15.14%, 13.78% and 10.72%, respectively. The above results indicate that the de-noising method is effective and can provide accurate IMU data for the following calculations.
To testify the validity of LSTM method, numerical simulations are performed by four methods: (1) pure INS (i.e., KF only executes time update process); (2) traditional artificial neural network with simple inputs (i.e., the inputs of ANN are current angular rate wbib and specific force fbib ); (3) traditional artificial neural network with complicated inputs [21] (i.e., the inputs of ANN are current and past 1-step angular rate wbib , specific force fbib and velocity VI ); (4) LSTM neural network with simple inputs (i.e., the inputs of LSTM are current angular rate wbib and specific force fbib ).
The system firstly works in the training mode, then we assume that the GPS signals are unavailable during the period of 1060 ~ 1120 s, and the system works in the prediction mode. It is worth mentioning that the more abundant the training samples, the more accurate the training model, and then it can predict accurately. Figure 6 is the prediction errors of position increments (i.e., ΔPG is Section 3.1) using different solutions. The RMSE values of longitude increment using simple ANN, complicated ANN and LSTM are 1.7795 m, 0.8539 m, and 0.1092 m, respectively. The RMSE values of latitude increment are 1.3186 m, 0.8191 m, and 0.1182 m, respectively. The results indicate that LSTM method can better establish inputs-outputs model and predict position increments more accurately than traditional ANNs.


FIGURE 6.
The prediction errors of position increments during 60 s GPS outages. (a) The prediction errors of longitude increment. (b) The prediction errors of latitude increment.
 
Figure 7 and Figure 8 present velocity and position errors of the four solutions during 60 s GPS outages, respectively, and Table 4 summarizes the corresponding maximum errors and RMSE values.
TABLE 4 The Error Statistics of Different Solutions During 60 s GPS Outages




FIGURE 7.
The velocity errors during 60 s GPS outages. (a) East velocity error. (b) North velocity error.
 


FIGURE 8.
The position errors during 60 s GPS outages. (a) Longitude error. (b) Latitude error.
 
To verify the effect of the proposed method under different movement states and outage time, another GPS outage is simulated. We assume that the GPS signal is unavailable during the period of 1600 ~ 1700 s. Figure 9 and Figure 10 illustrate velocity and position errors of the four solutions during 100 s GPS outages, respectively, and Table 5 summarizes the corresponding maximum errors and RMSE values. The results show that the LSTM method has the best navigation accuracy. Compared with complicated ANN, the maximum errors of velocity and position errors are decreased by 64.40%, 38.79%, 72.81% and 40.15%; the RMSE values are decreased by 62.07%, 41.02%, 69.54% and 41.87%. In addition, the inputs of LSTM are much less than that of complicated ANN. It is worth mentioning that the positioning errors during GPS outages can be affected by the movement states of the vehicle. As the movement state of outage-100s is simpler than that of outage-60s, the positioning errors of outage-100s are lower than that of outage-60s.
TABLE 5 The Error Statistics of Different Solutions During 100 s GPS Outages




FIGURE 9.
The velocity errors during 100 s GPS outages. (a) East velocity error. (b) North velocity error.
 


FIGURE 10.
The position errors during 100 s GPS outages. (a) Longitude error. (b) Latitude error.
 
From Figures 7–10 and Tables 4–5, it can found that four solutions show significantly different navigation accuracy: (1) pure INS performs the worst in these methods. For example, the maximum errors of position for second outage reach 48.1652 m and 16.8037 m. It can be attributed to the fact that the navigation accuracy decreases over time due to the inherent errors of IMU; (2) simple ANN performs better than the pure INS. The inputs of the model are current angular rates and specific forces, so this model is simple. Since the past useful information is not used, the effect of simple ANN is limited; (3) for the complicated ANN method, its navigation performance is greatly improved with respect to the simple ANN. For example, compared with the simple ANN, the RMSE values of longitude and latitude during 100 s GPS outages are decreased by 86.31% and 67.87%, respectively. Its inputs include present and past information of angular rates, specific forces and velocity. The algorithm is effective, but the model is more complicated; (4) the LSTM method has the best navigation accuracy. The RMSE values of longitude and latitude during 100 s GPS outages are decreased by 69.54% and 41.87%, respectively, with respect to complicated ANN. Moreover, the inputs of LSTM are much less than that of complicated ANN.
B. Real Road Tests
To further validate the proposed approach, real road tests are performed. The IMU uses the Ellipse-A of SBG SYSTEMS Company, whose sampling frequency is set to 100Hz. The GPS receiver uses the Trimble Company, and the frequency is 1Hz. Real-time kinematic GPS provides high precision navigation, which is taken as the reference values. Figure 11 shows the test vehicle with navigation system equipment, and Table 6 lists the characteristics of Ellipse-A IMU.
TABLE 6 Characteristics of Ellipse-A IMUs




FIGURE 11.
Test vehicle with navigation system equipment.
 
To evaluate the performance of the proposed method, simulated GPS outage is intentionally introduced by artificially removing GPS solution. As the accuracy of IMU is low, the pure INS will rapidly diverge in a short time, so the real road test assumes that there is a GPS outage for a length of 30 s during the period 220~250 s. It is worth mentioning that the IMU data used in following analysis are de-noising by the EMDTF. To maintain consistency with the simulations, the experimental tests are carried out on a road that is basically at the same height. Figure 12 and Figure 13 give the velocity and position errors, respectively. Table 7 summarizes the error statistics of four solutions.
TABLE 7 The Error Statistics of Different Solutions During 30 s GPS Outages




FIGURE 12.
The velocity errors during 30 s GPS outages. (a) East velocity error. (b) North velocity error.
 


FIGURE 13.
The position errors during 30 s GPS outages. (a) Longitude error. (b) Latitude error.
 
Figures 12–13 and Table 7 show that four solutions have different effects: (1) pure INS has the largest errors. For example, the maximum errors of east and north velocity reach to 30.7543 m/s and 14.7981 m/s, respectively; (2) simple ANN performs better than the first method. The maximum errors of east and north velocity are reduced to 3.6994 m/s and 3.9464 m/s, respectively; (3) for the complicated ANN method, its navigation accuracy is increased by a level compared with the simple ANN; (4) the LSTM method preforms best in the four solutions. The RMSE values of east velocity, north velocity, longitude and latitude are reduced by 21.79%, 14.85%, 55.03% and 19.66%, respectively, with respect to complicated ANN. Furthermore, the inputs of LSTM are six parameters while the inputs of the complicated ANN are eighteen parameters.
 C. Dijkstra Shortest Path Algorithm using Global Position System

Dijkstra Algorithm  
Dijkstra’s algorithm is invented by Dutch computer scientist Edsger Dijkstra in 1956 and published in 1959, is a graph based searching algorithm that solves the single source shortest path problem. It is applied only on positive weights graphs. This algorithm is often used in routing. Dijkstra’s algorithm is used for finding the shortest path with minimum cost. 
“For example:-Let vertices in a graph the cities &edges which link these vertices are the driving distances from one city to another city. DSPA is used to find the shortest route from one city to another with minimum cost. It solves only the problems with nonnegative costs, i.e., Cij >=0 for all (i, j) belongs to E, Where C is the cost & E is the edges for a graph. 
Global Positioning System (GPS) 
GPS is a satellite based system that can be used in navigation to locate the positions anywhere on the earth. GPS is designed & operated by U.S. Department of Defense (DOD).GPS consists of satellites, control & monitor stations and GPS receivers. GPS receivers take information which is transmitted from the satellites and uses triangulation to calculate a user’s exact location. GPS is used in a variety of ways: 
To determine the position of locations. 
To navigate from one location to another. 
To create digitized maps. 
To determine the distance between two points. 
 
Working of GPS 
The basis of GPS is a constellation of satellites that are continuously orbiting around the earth. These equipped with atomic clocks & transmit radio signals that contain their exact location, time and other information. The radio signals which are transmitted from the satellites are monitored & corrected by control stations which are sent back to satellites using ground antenna. The radio signals from satellites are picked up by the GPS receiver. A GPS receiver needs only 3 satellites to plot a rough, 2D position, which will not be very accurate. Ideally, 4 or more satellites are needed to plot a 3D position, which is more accurate than 2D [11]. 
Three Segments of GPS 
Space Segment 
Control Segment  
User Segment (see fig.1) 
 
Space segment: The satellites orbiting around the earth. 
Control segment: The control & monitoring stations. User Segment: The GPS receivers owned by civilians and military. 
 
          
Fig. 1 Three segments of GPS [15]
 
In this paper we use the GPS in Dijkstra’s algorithm for finding the current location. By using this position we calculate the distance from source to every node in the graph. From this we also estimate the shortest path. Distance is given by a formula: 
Distance= [(x2-x1)2 + (y2-y1)2+ (z2-z1)2]1/2 
 
Where x, y, z are the coordinates of a position given by GPS. In this paper we discussed about 1 is introduction, 2 is related work, 3 is proposed work, 4 is results and analysis,5 is conclusion and future work & 6is references. 
RELATED WORK 
GPS is used for tracking your vehicles & keeps regular monitoring. This tracking system can tell your location & that information can be observed from another remote location. This paper consists hardware part i.e. GPS,GSM,MAX 232,16*2 LCD &software part is used for interfacing all the required modules & a web application is also developed at client side. This is used for controlling theft of a vehicle. The simulation is done by PROTEUS software. It can be beneficial for: 
Parents to look after their children. 
To track animals in forest 
in delivery services 
in fire services & COP department. 
We have read about the bus monitoring using polyline algorithm. Day by day population is increases very fastly, which results in higher burden on public transportation. For a system is proposed in this paper. This system is developed using these technologies like GPS, Google Map & GPRS (Global Packet Radio Service) .the consists of GPS enabled device like mobile phones embedded in the bus, which find out its current coordinates periodically after some interval & send it to the database for the being processed & analyzed. Dijkstra’s algorithm is also used in this paper. 
The concept developed is focused on one of the most well known shortest path algorithm: the Dijkstra’s algorithm. Although the latter is sufficiently efficient for small network like a city sized one, its running time for country size or continental size geographical maps is prohibitive for real time application. This method is also applicable to other type of shortest path algorithms on graph network. The basic algorithm for this is the Dijkstra’s algorithm . 
A route planning project named planific@ is developed for the city of Madrid (Spain).its main objective is to develop an intelligent system that is capable of routing people from one place to other using public transport. For this we study the route planning algorithm for this. In this Dijkstra’s algorithm is also used for finding the shortest path. Planning Domain Definition Language (PDDL) is also used in this paper . 
Location based services offer many benefits to mobile user to retrieve the information about their current location & process that data to get more useful information near to their location. Using a GPS assisted phone & a web service using GPRS ,location based services can be implemented on Android based smart phones to provide services like advising client of current traffic conditions, providing routing information , helping them find nearby hotels. In paper location based services is implemented through Google Web Services & Walk Score Transit APIs on Android Phones to give multiple services to the user based on their location .  
The Real Time GPS Navigation System determines the user’s location on the digital map of Beirut using a GPS receiver. The user enters the destination and the shortest path is computed using Dijkstra’s algorithm. The application guides the user along the way by giving him/her directions. The user can take a different route and the corresponding shortest path is dynamically recomputed. However, no matter how accurate the GPS is, errors may occur; the GPS fails to show the correct user’s position. Corrections used in our application are based on pattern recognition techniques which take several previous GPS measurements to estimate the current position. Our Real Time GPS Navigation System was realized using innovative techniques. The shortest path algorithm, for example, is an improvement over Dijkstra’s classical algorithm. The driving directions are generated by analyzing the geometry of the map instead of using a table at each node. Finally, the correction of the GPS errors and their matching on the map are performed without requiring any radio signals; they rely only on the raw GPS signal and the geometry of the road network. Moreover, the system has a user-friendly interface that facilitates traveling in the city of Beirut . 




                                                          
                                    
Proposed Algorithm 
Step1: INITIALIZE d[s]=0 for all vєV   
{s},where s as source, V as set of all vertices.  
           Do d[v] =∞.                     //set all node’s distances to ∞ except s. 
Step2: Get the current position (x1, y1) of source node from GPS. 
           Source_x=x1; 
           Source_y=y1;            Dist.=0; 
Step3: S is the set of visited vertices. 
           Set S = φ                    //S is initially empty.             Q = V                            //Queue initially contain all the vertices. 
           While Q ≠ φ                 //while Q is not initially empty. 
           Do u = mindistance(Q,d)         //select element of Q with min. distance. 
           S = S U {u}                        //add u to the list of visited vertices.


BREADCRUMBS AND LOCATION PROFILES 
Some GPS navigation systems allow you to automatically store location information at periodic intervals allowing you to look back at where you’ve been and retrace your steps. The GPS location includes latitude, longitude and elevation. This location information can be plotted on various kinds of graphs as shown in Figures 2 and 3. Figure 2 shows a cross-sectional view with distance and elevation between two points while Figure 3 shows a bird’s eye view of location markers superimposed onto a map. The location markers on these graphs are sometimes called breadcrumbs.  
There is a significant amount of information stored in these location profiles. The relative speed of the vehicle is evident from the spacing of the markers. The closer the markers are to one another the slower the vehicle is moving. The distance between successive location points and the time difference is used to estimate the average speed between the points. Note for example in Figure 2 how the vehicle tends to move slower when going uphill and faster when going downhill. The distance between successive markers also shows how the vehicle accelerated and decelerated at different times.

SAMPLING AND PARSING OF ROUTE SEGMENTS 
To be useful the raw location data captured by the GPS system must be parsed to determine the time it took to traverse each route segment. The parsing of route segments can be illustrated in reference to Figure 3. From the location and spacing of the breadcrumbs it is possible to see that the vehicle entered from the lower left, stopped at the intersection and then took a left and then a right into the parking lot of the cactus café. The vehicle then circled around the parking lot and exited to the right. Later the vehicle returned and drove past the cactus café exiting the opposite way in which it arrived.  


FIG :- 2  Vertical Location Profile for Cajon Pass

FIG :- 3 Bird’s Eye View of GPS Location Markers

The time it took to traverse each route segment in Figure 3 can be obtained by parsing. The first step in parsing the route segments is to determine which route segment each breadcrumb corresponds to. Whenever two successive breadcrumbs fall on different route segments the time required to traverse the completed segment can be estimated by taking the corresponding recorded time values and interpolating between them. The accuracy will depend on the sampling interval (in Figure 3 the sampling interval appears to be on the order of once every few seconds). 

INTERPOLATION AND EXTRAPOLATION OF DATA  
   Each time a route is traversed it adds a new data point. Over the span of several months or years this can provide many values for each route segment.  This could represent, for example, the typical person driving to work every day. Besides distance many factors affect the time it takes to traverse a route segment. Besides distance many factors affect the time it takes to traverse a route segment.  
Besides distance many factors affect the time it takes to traverse a route segment. For example: 
traffic 
weather 
time of day 
time of year  
day of the week 
Rush hour traffic is usually asymmetrical. Usually there are more people going in one direction than the other, especially on highways in urban areas. There are also seasonal factors:  people going to the shore in the summertime, traffic congestion in the areas surrounding schools and universities when classes are in session, and certain holidays of the year can dramatically alter traffic patterns. This raises a number of
Rush hour traffic is usually asymmetrical. Usually there are more people going in one direction than the other, especially on highways in urban areas. There are also seasonal factors:  people going to the shore in the summertime, traffic congestion in the areas surrounding school and universities when classes are in session, and certain holidays of the year can dramatically alter traffic patterns. This raises a number of
                   
FIG :- 4 System Architecture

        interesting challenges including how best to extrapolate and interpolate the data. Suppose for example a given route segment took 9 minutes on a Monday night at 6pm and only 3 minutes on a Wednesday night at 12AM and it is desired to estimate how long it will take on Thursday night at 8PM. Using linear interpolation, it could be estimated that it would take 7 minutes on a Thursday night at 8PM. A different set of data might be used for weekends as well as for holidays as dates of major holidays are known and can be programmed into the system. Data from previous holidays could override the day of week information. This would be an example of dynamic data clustering. Extrapolation could also be used when data from one route segment is used to make an estimate for a route segment that had never been previously traversed.

FEATURE EXTRACTION 
The use of actual measured data in route planning can provide significant improvements in choosing an optimal route. However, there is more information in the data that can be used to model not just the time to traverse the route segments but also the transitions between route segments. This can be called feature extraction. In going from starting point to destination it is generally necessary to stop many times along the way. Typical places to stop are at road or segment transitions and terminations.  Each route segment has some termination for example: 
traffic lights 
stop signs 
yield signs  
nothing 
Knowing whether there is a stop sign or traffic light at an intersection could make a significant difference in determining an optimal route. Velocity profiles can be analyzed to extract this type of feature information. The distance between successive markers shows how the vehicle accelerated and decelerated at different times. For example, in Figure 3 it is not clear whether there is a stop sign or traffic light at the first intersection. However, after this segment has been traversed several times a pattern might start to develop. If the vehicle stops half the time and goes through without stopping the other half of the time it might be deduced that there is a traffic light at that intersection.  

SYSTEM ARCHITECTURE AND OPERATION 
It is assumed that the system operates as an overlay to an existing GNS and that the underlying system has all roads and highways represented in a database of route segments. It is also assumed that each segment can be identified by the GPS coordinates of its endpoints or some other unique identifier. The entire system of roads and highways is assumed to be a connected graph G(V,E). Every vertex in the graph corresponds to the termination point of at least one route segment. A shortest path algorithm can used to determine the optimal route between a starting point and destination  . The information stored by the GPS is as follows:   
GPS location and time at periodic intervals 
time and dates each segment traversed 
time to traverse segment  
direction of traversal 
The overall architecture of the system is shown in Figure 4. Raw GPS data is collected and archivally stored for future route segment parsing and feature extraction. Route segments are periodically parsed and stored in a separate database. When it is desired to calculate an optimal route between two points the interpolator/extrapolator uses the stored data and the current date and time to estimate the time required to traverse each segment and this data is fed into the shortest path algorithm. Once this calculation is made it will be necessary to go back and repeat the extrapolation/interpolation process for each segment based on the estimated time of arrival to the beginning of each segment and this data fed once again into the shortest path algorithm. This process is repeated until it converges. It would be inaccurate to estimate the time to traverse each segment based on the time at the start of the trip. The time to traverse each segment should be estimated based on the time it will be when traversing the segment.  It is assumed that a typical GNS gives the user a choice between different modes of operation including but not limited to:   
Shortest distance 
Fastest Time  
Most use of Freeways 
Least use of Freeways 
The difference between the first two options, shortest distance and fastest time, is that the fastest time option makes some assumption about the type of road and how fast you are likely to be traveling on that road. There is apparently some model built into commercial GNS systems which categorizes the type of road and uses it to estimate the speed of travel on that type of road and hence the time of traversal. Distance is the primary factor to optimize but it is only one factor and is assumed to be fixed and independent of when the travel occurs. Most people care more about the time it takes them to get where they are going than the actual distance and this can vary significantly at different times of the day, week and year. This is apparently not reflected in typical GNS systems and so it is proposed to add a fifth mode to the above list called “Experience” mode. Experience Mode is the same as fastest time except that actual measured data is used to estimate the time for each route segment. Experience mode operates exactly the same as the Fastest Time mode except it uses the measured and extrapolated data as shown in Figure 4. It has no effect on the other operating modes.     
The system would operate as follows. At some periodic interval (for example every 10 seconds) the system would record GPS location information and the time and the date. This interval could also be made variable to assist in feature extraction, taking more frequent samples when the vehicle is accelerating or decelerating. The data could also be compressed during long intervals of highway driving on cruise control. At some predetermined interval the system would independently process the raw GPS data to parse it into route segments and perform feature extraction. This could be for example once per day at midnight or after every trip completion or perhaps even after each route segment completion.  
The first time the experience mode is used it has no data and so it relies completely on the default data that has already been stored for the fastest time. The first trip gives one data point for some subset of all the route segments and is simply stored for future reference. The GPS data for the completed route is parsed and the time of traversal for each segment is stored. The next time a trip is planned the measured data is used to replace the default route segment traversal time stored in the system for any applicable route segments. The assumption is that the actual measurements are more accurate than the original stored data. After the second trip the GPS data is processed as before and so forth for each trip thereafter. At some point there will be two or more measured data values for some subset of the route segments and at that point interpolation/extrapolation can be used. As more and more trips are made at different times of the day, week, month and year the accuracy of the interpolation/extrapolation should improve by experience. Velocity and acceleration profiles from traversed route segments can be extrapolated to predict the time to traverse previously untraversed route segments. As time goes on more data points are collected at different times of day and different days of the week. At first all of the data is used, and each new data point should give more validity to the overall model. However, as more data is collected it might be more accurate to look at subsets of the data. Exactly when and how to evolve to the data clustering is something that needs to be determined (as discussed in section 4). Using all the available data all of the time also makes it more difficult for the system to adapt to changing or temporary circumstances.   

RESULT AND DISCUSSION 
    According to results in Table 9, the Reference Stations Network proposed by Wübbena  to improve the accuracy of GPS can reduce only two factors that affect the accuracy of GPS. For the Kalman Filter Algorithm which was used by Qi and Malleswari, managed to mitigate four factors that affect the accuracy of GPS whereas for PGPS which used by Chung [, only three GPA inaccuracy factors can be rectified. Map-Matching Algorithm which was applied by Alain  and the Google Map GPS Tracking Enhancement explored by Line does not have any impact on the listed factors that affect the accuracy of GPS. However, both of these methods could improve the GPS tracking activities in other ways such as effective interface on map applications. Hence, the most effective method which can improve the accuracy of GPS is the Kalman Filter Algorithm used by Qi and Malleswari . PGPS and Reference Stations Network can be suggested as alternative methods to improve the GPS accuracy as well. According to Malleswar, the Kalman Filter Algorithm is a linear recursive filtering method which can be applied to smoothen the location coordinates data obtained by the GPS receiver. Besides that, when the location coordinates of the GPS user is being estimated, this algorithm can boost the accuracy of GPS by reducing the estimation error to the lowest value. 
 




Table 9.  Overall existing methods and the inaccuracy factors that could be mitigated  
 


SUMMARY AND CONCLUSIONS 
An architecture for a learning based artificial intelligence overlay to an existing GPS Navigational System (GNS) is discussed. It uses actual measured GPS location, date and time information to improve the performance of optimal route determination. The system recognizes that besides distance, many factors affect the time required to travel between two points including: traffic, traffic lights, stop signs, individual driving habits, weather, direction of travel, day of week and time of year. The underlying reality is a very complex and dynamic system about which only partial information is available. The system operates by taking measured GPS data for a completed route and parsing it into route segments and using interpolation and extrapolation to estimate the time it took to traverse the segment. This can then be used for feature extraction creating a model which is more accurate than the default data. The more data the better the performance of the system should be in terms of the accuracy of prediction. In other words, the system would learn by experience. This raises a number of challenges including how best to extrapolate and interpolate the data and what subsets of the data to use (dynamic data clustering). The goal is to make the system completely autonomous and not dependent on any user input whatsoever. It is designed so that an open source prototype could be developed to allow the algorithms can be tested and evaluated. The goal is to build a system that learns over time and continues to improve in a manner analogous to how a human being might improve based on a perfect memory of all past experiences.   

REFERENCES 
 
Lin, J.Y, Yang, B.K., Tuan A.D., and Chen, H.C. (2013). “The Accuracy Enhancement of GPS Track in Google Map”, 2013 Eighth International Conference on Broadband and Wireless Computing, Communication and Applications, Compiegne, France. pp. 524-527. 
Iqbal, A., Mahmood. H., Farooq, U., Kabir, M.A. and Asad, M.U.. (2009). “An Overview of the Factors Responsible for GPS Signal Error: Origin and Solution”, 2009 International Conference on Wireless Networks and Information Systems, Shanghai, China. pp. 294-299. 
Bajaj, R., Ranaweera, S.L., Agrawal, D.P.. (2002). “GPS: Location-tracking Technology”, Computer, vol.35, no..4, pp. 92-94. 
Huang, J.Y., and Tsai, C.H.. (2008). “Improve GPS Positioning Accuracy with Context Awareness”, 2008 First IEEE International Conference on Ubi-Media  Computing, Lanzhou, China, pp. 94-99. 
Wubbena, G., Andreas, B., Seeber, G., Boder, V. and Hankemeier, P., (1996). “Reducing Distance Dependant Errors for Real-Time Precise DGPS Applications by Establishing Reference Station Networks”. In Proceedings of the 9th International Technical Meeting of the Satellite Division of the Institute of Navigation (ION GPS-96) 
Enge, P., Walter, T., Pullen, S., Kee, C., Chao, Y. and Tsai, Y.  (1996). “Wide area augmentation of the global positioning system”. Proceedings of the IEEE, vol. 84 Aug. 1996, pp. 1063–1088. 
Qi, H. and Moore, J. B. (2002). “Direct Kalman Filtering Approach for GPS/INS Integration”, IEEE Trans. Aerosp, Electron. System. vol. 38, no. 2, 2002, pp. 687-693. 
Malleswari, B.L., MuraliKrishna, I.V., Lalkishore, K., Seetha, M., Nagaratna, P. H. “The Role of Kalman Filter in the Modelling of GPS Errors”, Journal of Theoretical and Applied Information Technology, pp. 95-101. 
White, C.E., Bernstein, D. and Kornhauser, Alain L.. (2000). “Some map matching algorithms for personal navigation assistants”. Transportation Research Part C, No. 8, 2000, pp. 91-108. 
 


