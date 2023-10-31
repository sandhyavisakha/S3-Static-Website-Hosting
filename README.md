# Setting up a Static Website on AWS S3 with Custom Domain
This guide will walk you through the steps to host a static website on Amazon S3 and associate it with a custom domain using AWS Route 53. In this example, we'll use the domain name "movetocloud.xyz."

## Getting Started

Steps:

1. Create an S3 bucket with the same name as your custom domain name, which in my case is “movetocloud.xyz", and upload an index.html file to the bucket
2. Under the bucket properties tab, enable static website hosting and select index.html file
3. Now in the permissions tab, add a bucket policy that allows public read access to the objects stored in the S3 bucket
4. Test the website by using the S3 object URL and it should work.
5. Now, in order to redirect the domain name "movetocloud.xyz" to the S3 bucket, create a record under the domain name in the Route 53 hosted zone, so that the bucket will be connected to the domain name. Using the simple routing policy, create a record and choose the endpoint as S3 bucket endpoint
6. Finally, the changes reflect and using the domain name “movetocloud.xyz”, I was able to view my website hosted on S3
