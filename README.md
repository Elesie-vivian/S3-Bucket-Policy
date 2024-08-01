# S3-Bucket-Policy

## SUMMARY

This Project explores S3 Bucket Policies and Access Control on AWS.It walks us through creating an S3 bucket, defining a bucket Policy to manage access permissions 
This process therefore gives a hands-on understanding of a JSON -formatted bucket policy and the elements contained within.

We also test the policy configuration by uploading objects to the bucket and retrieving them.


### Creating an S3 Bucket
We configure an S3 Bucket called "dollybucket456" and review Documentation on Amazon S3 Bucket Policies

![alt text](<Images/Image 1.PNG>)

### Policy Configuration
We configure a JSON-formatted Policy to specify the permission allowed in the bucket

![alt text](<Images/Image 2.PNG>)

### Testing Access Control
First, we upload an object to our S3 bucket using the AWS management console,then attempt to retrive the object from various scenarios and observe the effect of access control

![alt text](<Images/Image 3.PNG>)

Attempting to retrieve the object in the bucket further shows the effect of access control and security tools available in a bucket.
**Using an allowed IP address:** This requires that you allow public access to your bucket to make the Bucket contents public and then share the bucket URL to whomever you allow access. This is achieved by unchecking the "Block Public Access" Button in Properties.

**Using a restricted IP address:** This requires a Pre-signed URL that grants temporary access to an object within a specific time period without necessarily altering the permissions settings of the Bucket. To achieve this, we select the object, then click on 'Actions', presigned URL, select the time duration to allow access and then copy the temporary URL generated.

**IAM users:** This permission must be specified in their IAM Policy to “GetObject” and the S3 bucket they want to access must allow access for this retrieval in its own policy.

Object retrieved from all three scenarios is as seen below

![alt text](<Images/Image 4.PNG>)


