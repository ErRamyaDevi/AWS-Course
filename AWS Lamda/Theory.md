## AWS LAMBDA
+ AWS is an event-driven, serverless function as a service provided by Amazon as a part of Amazon web services. It is designed to enable developers to run code without provisioning or managing servers. It executes code in response to events and automatically manages(scales up) the computing resources required by that code.
+ lets you run code without thinking about servers.
 ### Lambda Function:
## What is Lambda?
+	AWS lambda is a serverless function managed by total AWS.
+	Pay- per-use
+	Automatically scaled up by AWS lambda- scaling done be vertical scaling i.e., when receiving high traffic, it will be scaled up vertically by required resources(CPU,Disk,Memory etc..)
+	Highly available.
+	Supports for multiple languages.

Cold start latency: after idle state, first time start, there will be a small latency.
Execution Time Limits
Stateless Execution Environment
Limited Execution Environment 

Example: Netflix

movie1.raw ->8k
Using Lambda, it will flatten the resolution according to the device we are accessing. mobile ->720p mp4, TV->4k , lap->1080p

![image](https://github.com/user-attachments/assets/5be7c397-581f-4bbd-af44-27bf06475879)

![image](https://github.com/user-attachments/assets/d44f514a-ccf9-4d46-908f-b1ced0e6f414)

## IAM Role: 
#### Though Lambda is a asset of AWS, communication between AWS resources only takes place through IAM Role.
