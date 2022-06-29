# JMeter_POC

### Summary
In UI mode considered 3 sets of Request which require authorization. 
Created separate transaction controller and included the request.
Used listener such as view result tree, summary report and aggregate report.
There are various other listners which we can integrate.
These are for Reporting purpose. 

Test Plan – Here, we can define user variable which will be capture during performance run

Thread Group – In this we can configure the performance workload – like number of users, ramp up and loop count. I also have the duration logic where we need to provide time in seconds

HTTP Sampler – I have used few HTTPS request in our POC which include Authorization, Add HCHB, add OTP visit and Partner mock server. In this we are passing the method type, path, body and base URL of the API

Different Element of JMeter – I have used Json Extractor for storing the token and sending It to subsequent request and CSV Data Set Config for storing the parameter and sending it during run time. We have lot of other JMeter element which we can include in JMX test plan. 

We can create separate JMX for each API and include in MasterTestPlan by using include controller

#### Command to run through Terminal
` $ jmeter -n-t Performance_test_script.jmx `
