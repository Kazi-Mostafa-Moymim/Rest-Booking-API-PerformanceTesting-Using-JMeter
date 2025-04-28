# Rest-Booking-API-Performance-Testing-Using-JMeter
This project demonstrates Performance Testing using JMeter, providing a collection of tests to validate various endpoints of the API.

## Features
* Tests for GET, POST, PUT, DELETE requests
* Collection of tests covering different API endpoints

## Technology used:
- JMeter

## Overview
This repository contains a JMeter project for performance testing of the [Restful-Booker](https://restful-booker.herokuapp.com/apidoc/index.html) Website.

## Usage
1. Clone the repository to your Local Machine From:
````
https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter.git
````
2. Open JMeter and load the test plan.
3. Configure the necessary settings and parameters in the test plan.
4. Run all Test plan.

## Run in CMD (Non GUI mode) on your project folder
1. To run the test plan through CMD (Non GUI mode), use the following command:
    ````
    jmeter -n -t Restfull_bookerT.jmx -l report\Restfull_bookerT.jtl
    ````
This command runs JMeter in non-GUI mode (-n), specifies the test plan file (-t), and writes the results to a JTL file (-l).

2. To run the test plan through CMD (GUI mode), use the following command:
    ````
    jmeter -g report\Restfull_bookerT.jtl -o report\Restfull_bookerT.html
    ````
This command runs JMeter in GUI mode (-g), making report to htl file (-l), and writes the report results to a html file (-l).

## Testing
The sample test plan includes the following components:
1. Thread Group:
    * Thread Count: 10
    * Ramp-Up Time: 10 second
    * Explanation:
       * Thread Count: Represents the number of virtual users (threads) executing the test concurrently.
       * Ramp-Up Time: Represents the time taken for all threads to start executing.
2. HTTP Proxy Server:
    * Used for recording the script of sample pages.
3. Logic Controllers:
    * Loop Controllers:-
       * Loop Count: 01
4. Config Eelements:
    * http header manager
    * json extractor
5. Listeners:
    * view result trees
    * summary report
    * aggrigate report
6. Save and Run the test plan
7. Execution:
    * Run all the test plan sequentially
    * you can start your execution with 100 thread group until error rate is 1.0%
8. Point to explore:
    * Running through CMD (Non GUI mode).
    * Running through CMD (GUI mode) for generating html report.
## Report 
1. 1000 Concurrent Request with 01 Loop Count; Avg TPS for Total Samples is ~ 100 And Total Concurrent API requested: 7000.
       ![1000](https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter/blob/cc1a7e5dc61d7de55384005b5a3718f4f588b8e3/Screenshot/1000.png)
2. 1500 Concurrent Request with 01 Loop Count; Avg TPS for Total Samples is ~ 150 And Total Concurrent API requested: 10500.
       ![1500](https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter/blob/cc1a7e5dc61d7de55384005b5a3718f4f588b8e3/Screenshot/1500.png)
3. 2000 Concurrent Request with 01 Loop Count; Avg TPS for Total Samples is ~ 200 And Total Concurrent API requested: 14000.
       ![2000](https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter/blob/cc1a7e5dc61d7de55384005b5a3718f4f588b8e3/Screenshot/500.png)
4. 2500 Concurrent Request with 01 Loop Count; Avg TPS for Total Samples is ~ 250 And Total Concurrent API requested: 17500.
       ![2500](https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter/blob/cc1a7e5dc61d7de55384005b5a3718f4f588b8e3/Screenshot/2500.png)
5. 2900 Concurrent Request with 01 Loop Count; Avg TPS for Total Samples is ~ 157 And Total Concurrent API requested: 20300.
       ![2900](https://github.com/Kazi-Mostafa-Moymim/Rest-Booking-API-PerformanceTesting-Using-JMeter/blob/cc1a7e5dc61d7de55384005b5a3718f4f588b8e3/Screenshot/2900.png)
### While executed 2900 concurrent request, found  3160 request got connection timeout and error rate is 18.16%. 
### Summary: Server can handle almost concurrent 16800 API call with  zero (0) error rate.

