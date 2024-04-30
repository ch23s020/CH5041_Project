# CH5041_Project
Course Project


Scheduling of Preventive maintenance: - A stochastic data-driven Approach to Study Sensor Failure Analysis and Cost Comparison. 

 

This Report has following parts: - 

    Introduction 

    Code Functionality: - Data Generation, Analysis, Visualization 

    Data Analysis:- Terminologies, Visualization, Graphs 

    Cost Analysis:-  Terms, Cost Comparison 

    Results 

    Conclusion 

    Future Perspective. 

 

    Introduction 

 

Today it is a pressing challenge before industries to optimize the plant operations. One of the focus areas is increasing the efficiency of the plant so to achieve the designed capacity and output. Heavy investments are made in capturing real time data through Manufacturing Execution System (MES) to enable executives and engineers for better planning and optimization throughout the layer of automations. One of the key concerns is incidental failures of instruments and the cost incurred on such failure maintenance. Such failures sometime have critical impact such as entire loss or halt in production systems. As the failure of instruments is stochastic in its very nature, hence gives an opportunity to model it through captured real time data on stochastic pattern for preventive maintenance and thereby securing the efficiency in plant operations. 

The goal of this project is to analyze the failure patterns of sensors using stochastic processes and visualize the distribution of failure days among the sensors and thereby develop a predictive maintenance strategy to optimize maintenance costs while ensuring operational efficiency. The analysis includes generating failure days for each sensor, calculating the frequency of failures, and comparing the costs of fixed-time maintenance and preventive maintenance strategies. 

This report provides an overview of the code functionality, data generation process, analysis of failure days and visualization of the results. 

    Code Functionality 

The code is written in Python and utilizes the NumPy and Matplotlib libraries for data generation, analysis, and visualization. 

    Data Generation: 

    The code generates failure days for each sensor from an exponential distribution with a specified rate parameter. The rate parameter is a hyperparameter that decides the distribution spread of the failure. Here we have assumed a = 0.10. 

 

    We used random. Exponential() library inbuilt for data sampling. To ensure the reproducibility we have fixed Random seed. The data generated using different random seed is collected in a separate spreadsheet to reproduce the same results using a data driven approach. 

 

    The failure days indicate the time duration after which each sensor is expected to fail. These failure days are sampled from an exponential distribution. In real time data scenario, we will use the standard plots from the data and sample accordingly. 

 

    E.g. Failure Days for Each Sensor: [ 3.21894941, 10.19516752, 9.77898119, 15.05268489, 6.50305204, 31.97454055, 59.65487573, 17.86851193,  2.27961454, 1.43928111] 
     

    The first sensor is expected to fail after approximately 3.22 days. 

    The second sensor is expected to fail after approximately 10.20 days. 

    The third sensor is expected to fail after approximately 9.78 days. 

    The fourth sensor is expected to fail after approximately 15.05 days. 

    The fifth sensor is expected to fail after approximately 6.50 days. 

    The sixth sensor is expected to fail after approximately 31.97 days. 

    The seventh sensor is expected to fail after approximately 59.65 days. 

    The eighth sensor is expected to fail after approximately 17.87 days. 

    The ninth sensor is expected to fail after approximately 2.28 days. 

    The tenth sensor is expected to fail after approximately 1.44 days. 

 

 

 

 

 

    Analysis: 

    Calculated the frequency of failure for each sensor, providing insights into the distribution of failure days among the sensors.  

 

        E.g. Frequency of Failure for Each Sensor: [0 1 1 1 0 0 1 0 0 1 1 0 0 0 0 1 0 1 0 0] 

	 

    Index 0: 0 sensors are expected to fail within the range of 0-1 days. 

    Index 1: 1 sensor is expected to fail within the range of 1-2 days. 

    Index 2: 1 sensor is expected to fail within the range of 2-3 days. 

    Index 3: 1 sensor is expected to fail within the range of 3-4 days. 

    Index 4: 0 sensors are expected to fail within the range of 4-5 days. 

    Index 5: 0 sensors are expected to fail within the range of 5-6 days. 

    Index 6: 1 sensor is expected to fail within the range of 6-7 days. 

    Index 7: 0 sensors are expected to fail within the range of 7-8 days. 

    Index 8: 0 sensors are expected to fail within the range of 8-9 days. 

    Index 9: 1 sensor is expected to fail within the range of 9-10 days. 

    Index 10: 1 sensor is expected to fail within the range of 10-11 days. 

 

 

 

    Sorts the sensors based on their failure days to identify the order of failure. As mentioned above the failure days, they are sorted to understand te failure order to schedule a preventive maintenance for respective sensor. 

 

    Visualization: 

	We have total three visualization plot as per following: 

 

    Plot of the sorted failure days and sorted sensors to understand the order of failure. (Second and third Plot Image1:- Graph:- RS_82 ) 

 

    The frequency of failure for each sensor, providing insights into the distribution of failure days among the sensors.( First Plot Image1:- Graph:- RS_82 ) 

 

    Generates exponential decreasing curves to visualize the probability of failure for each sensor over time. (Image2) 

 

 

 

 

 

3. Data Analysis 

    Terminologies 

    Failure Days for Each Sensor 

The failure days for each sensor indicate the expected time duration (in days) before each sensor is likely to fail. The data reveals varying failure times among the sensors, with some sensors expected to fail earlier than others. This shows the possibility of scheduling the preventive maintenance instead of fixed or routine maintenance. 

    Frequency of Failure for Each Sensor 

The frequency of failure for each sensor provides insights into the distribution of failure days among the sensors. It indicates how many sensors are expected to fail within specific ranges of failure days. 

    Visualization 

I) Distribution of Failure Days 

    The histogram visually represents the distribution of failure days among the sensors. It provides a clear understanding of when failures are expected to occur more frequently. 

    Histograms to visualize the distribution of failure days. (Frequency Vs Failure Day): 

    Each bar in the histogram represents a range of failure days (bin). 

 

    The height of each bar indicates the number of sensors that are expected to fail within that range of days 

    e.g.:-  From above mentioned array of data for Random seed 82, We have five sensors failing between 1 to 10th day. From the following plot one can see that total numbers of sensor failure are five hence conforming to our analysis (First Plot) 

 

 

Image1:- Graph:- RS_82 

 

 

II) Sorted Failure Days of Sensors 

The plot shows the failure days of sensors sorted in ascending order. It helps identify the order in which sensors are expected to fail, with sensors having earlier failure days appearing towards the left of the plot. 

III) Exponential Decreasing Curve for Probability of Failure 

The exponential decreasing curves visualize the probability of failure for each sensor over time. It demonstrates how the probability of failure decreases exponentially as time progresses.  

 

					Image2 :_Sensor failure Graph. 

 

4. Cost Analysis 

The purpose of this estimation is to analyze the failure patterns of sensors in a system and thereby determine the effectiveness of preventive maintenance using the following step by step approach. 

1. Failure Pattern Analysis (As discussed in above sections in detail) 

    Data Generation: Simulated failure days for each sensor using an exponential distribution to model the failure patterns realistically. 

 

    Frequency Analysis: Calculated the frequency of failures for each sensor to understand the distribution of failure occurrences. 

2. Cost Comparison 

    Cost Analysis: Here by comparing the costs of fixed-time maintenance and preventive maintenance strategies for different scenarios, we found that preventive maintenance is cost effective. The scenario here refers to the different values of random seed. For instance, our earlier plot shows random seed (RS_82) and Image 3 is the comparison for the cost for the same. To incorporate the different failure scenarios and comparison, we will include some more data generated by changing the value of random seed.   

 

    This analysis involved calculating the total costs incurred for each strategy, including maintenance costs and failure costs. 

 

Following are the details and assumptions made on cost: - 

 

working_capital = 100000  # Working capital of the plant 

 

failure_cost_per_sensor = 5000  # Cost incurred per sensor failure (in rupees) 

 

fixed_maintenance_cost_per_sensor = 2000  # Cost incurred for fixed-time  

maintenance per sensor (in rupees) 

 

preventive_maintenance_cost_per_sensor = 1000 # Cost incurred for preventive maintenance per sensor (in rupees) 

 

# Calculate cost of fixed-time maintenance for all sensors 

 

fixed_maintenance_cost_all = fixed_maintenance_cost_per_sensor * len(failure_days) 

 

 

# Calculate total cost of failure for fixed-time maintenance 

failure_cost_all = failure_cost_per_sensor * len(failure_days) 

 

# Calculate total cost of failure for preventive maintenance 

failure_cost_failing = failure_cost_per_sensor * sum(failure_frequency) 

 

# Calculate total costs in rupees 

total_cost_fixed_maintenance = fixed_maintenance_cost_all + failure_cost_all 

total_cost_preventive_maintenance = preventive_maintenance_cost_failing + failure_cost_failing 

 

# Calculate savings from preventive maintenance 

savings = total_cost_fixed_maintenance - total_cost_preventive_maintenance 

 

 

	 

5. Results 

I) Failure Pattern Analysis 

    Failure Days Distribution: The failure days for each sensor were distributed according to an exponential distribution, with varying time durations until failure. 

 

    Scope for Preventive Maintenace: We observed that certain sensors were more prone to failure than others, indicating potential areas for targeted maintenance. 

II) Cost Comparison 

    Total Costs: The total costs of fixed-time maintenance and preventive maintenance strategies were calculated for each scenario. 

 

    Savings: By implementing a preventive maintenance strategy targeting failing sensors, significant cost savings were achieved compared to fixed-time maintenance. 

 

			Image 3:- Cost Comparison for one Scenario (RS_82) 

 

 

Image 4:- Cost Comparison for different Scenario 

6. Conclusion 

Based on the analysis of failure patterns of sensors using stochastic processes. By analyzing the distribution of failure days and visualizing the results, it helps in understanding the reliability and maintenance requirements of sensor systems. Hence, we can recommend implementing a predictive maintenance strategy that targets failing sensors identified through failure pattern analysis. This approach minimizes maintenance costs while maximizing operational efficiency by addressing potential failures proactively. 

7. Future Considerations 

    Real-time Monitoring: Currently, MES (Manufacturing Execution Systems) are being used for Realtime data collection and analysis. This approach can be integrated with the collected data for cost efficient operation of industries. 

 

    Machine Learning Models: Developing machine learning models can enhance predictive maintenance capabilities by identifying subtle patterns in sensor data. 

 

 
