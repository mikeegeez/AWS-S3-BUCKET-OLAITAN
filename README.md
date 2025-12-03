# AWS-S3-BUCKET-OLAITAN
http://olaitan-portfolio-static-website.s3-website-us-east-1.amazonaws.com

As part of my Cloud Engineering training at Tech Crush, I was tasked with deploying a static website using Amazon S3.
To begin, I created the website structure using Claude.ai and customized it to make it more personal adjusting the colors, modifying the headers, and editing the contact page to reflect my brand on visual Studio code.


I then logged into the AWS Management Console, selected my preferred region, and created a new S3 bucket. During the setup, I provided a unique bucket name and initially kept the “Block All Public Access” settings enabled.

Become a member
Next, I enabled Static Website Hosting under the Properties tab and specified my index.html file as the entry point. After that, I uploaded my index.html file to the bucket through the Objects tab.

To make the website publicly accessible, I added a JSON bucket policy under the Permissions tab. This policy grants public read access to the objects in the bucket which is required for S3 static website hosting.Challenges Encountered

When I first attempted to deploy the website, it did not load.
The website endpoint returned the following error:

Press enter or click to view image in full size

403 Forbidden
Code: AccessDenied
Message: Access Denied
...
An Error Occurred While Attempting to Retrieve a Custom Error Document
Code: AccessDenied
Message: Access Denied
Resolution
Press enter or click to view image in full size

Upon reviewing my configuration, I discovered that I had not updated the bucket policy correctly to allow public access. After adding the appropriate JSON policy and redeploying, I reloaded the website using the S3 Website Endpoint. This time, the site loaded successfully.
