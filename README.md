# Perfromance_Testing
## Features

- Load testing Report
- Summary
- Introduction
- Install
- Prerequisites
- Elements of a Minimal Test Plan
- Test Plan
- Collection of API
- Make jtl File
- Make html File
- HTML Report
- Stress Testing
- Spike Testing

## Load testing Report

| Concurrent Request  | Loop Count | TPS| Error Rate|  Total Concurrent API
| :------------ |:---------------:| -----:|       | ---------|     -------
| 200  | 1 | 10 |  0%  |  600        | 
| 500  | 1 | 25 |  0%  | 1500         | 
| 1000 | 1 | 50 |  0%  |   3000       | 
| 1500 | 1 | 75 |  0%| 4500 | 
| 1560 | 1 | 78 |  0.13% | 4680 | 
| 1575 | 1 | 77 |  1.71%| 4725 | 


## Summary

- While executed 1560 concurrent request, found 4680 request got connection timeout and error rate is 0.13%.
- Server can handle almost concurrent 1550 API call with almost zero (0) error rate.


## Introduction

This document explains how to run a performance test with JMeter against an Demo Site.


## Install 
Java :
https://www.oracle.com/java/technologies/downloads/

JMeter :
https://jmeter.apache.org/download_jmeter.cgi

Click =>Binaries
=>apache-jmeter-5.5.zip

## Prerequisites

- As of JMeter 4.0, Java 8 and above are supported.
- we suggest multicore cpus with 4 or more cores.
- Memory 16GB RAM is a good value.

## Elements of a minimal test plan
- Thread Group

- The root element of every test plan. Simulates the (concurrent) users and then run all requests. Each thread simulates a single user.

- HTTP Request Default (Configuration Element)

- HTTP Request (Sampler)

- Summary Report (Listener)
## Test Plan
Testplan > Add > Threads (Users) > Thread Group (this might vary dependent on the jMeter version you are using)

- Name: Users

- Number of Threads (users): 200 to 1575

- Ramp-Up Period (in seconds): 10

- Loop Count: 1

## Collection of API
I used demo website here . But you can collect API by running Blazemeter and save it to JMX file.

## Test execution (from the Terminal)
- JMeter should be initialized in non-GUI mode.
- Make a report folder in the bin folder.
- Run Command in jmeter\bin folder.

## Make jtl file
- jmeter -n -t demo_test_200.jmx -l report\demo_test_200.jtl
Then continue to upgrade Threads(200 to 1575) by keeping Ramp-up Same.
![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/make_JTL_file.png?raw=true)
![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/JTL_file.png?raw=true)

After completing this command
## Make HTML File
- jmeter -g report\demo_test_200.jtl -o report\demo_test_200.html
![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_file_200.png?raw=true)
# HTML Report
Number of Threads 200 ; Ramp-Up Period 10s 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_200.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_200.png?raw=true)  |

Number of Threads 500 ; Ramp-Up Period 10s 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_500.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_500.png?raw=true)  |

Number of Threads 1000 ; Ramp-Up Period 10s 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_1000.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_1000.png?raw=true)  |

Number of Threads 1500 ; Ramp-Up Period 10s 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_1500.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_1500.png?raw=true)  |

Number of Threads 1560 ; Ramp-Up Period 10s 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_1560.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_1560.png?raw=true)  |


## Stress Testing
Stress Testing is a type of software testing that evaluates how the software responds under extreme conditions. It verifies how robust a system will be, and its response capabilities and error handling when it is subjected to conditions where its normal functioning can be compromised.

#### Number of Threads 1575 ; Ramp-Up Period 10s
 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_1575.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_1575.png?raw=true)  |

## Spike Testing

Spike testing is a type of performance testing where the demand for an application is suddenly and drastically increased or decreased. Spike testing's objective is to ascertain how a software program will behave under highly variable traffic conditions.

#### Number of Threads 1600 ; Ramp-Up Period 10s
 
| Requests Summary  | Error|
| ------------- | ------------- |
| ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/html_report_1600.png?raw=true)  | ![App Screenshot](https://github.com/Abdullah-SWE-171/Perfromance_Testing/blob/main/image/error_1600.png?raw=true)  |

## Feedback

If you have any feedback, please reach out to me at abdullahabir183@gmail.com

