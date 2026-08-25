# Host a Website on Amazon S

**Author:** Kevin Carl Ricafort  
**Email:** kevincarlricafort1@gmail.com

---

![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I am demonstrating how to deploy and host a scalable static website using Amazon S3, featuring bucket configuration, public access controls, and custom static hosting settings.

### Tools and concepts

In this project, I learned how to use Amazon S3 in hosting static websites. In addition, I learnt the nuances of S3 components like buckets and objects. 

### Time, challenges, and wins

This project took an hour to make. In this project, the most complicated part was the troubleshooting part and managing my composure after encountering such errors. 

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I am going to use Amazon S3 to create a storage space for my website files. 

### How long it took to create the bucket

In fact, creating an S3 bucket is nearly instantaneous since it typically under a second for the API call itself. Moreover, the bucket is available for an immediate use after the call returns successfully. 

Note to also consider these few factors in creating an S3 bucket:
1. Network Latency
2. Initial configurations like IAM and bucket policies, versioning, or encryption at creation time. 

### Region selection

For this project, I chose Asia Pacific (Singapore) ap-southeast-1 to minimize the latency. 

### Understanding bucket name uniqueness

S3 buckets must have a globally unique name, meaning no two S3 buckets anywhere in the world can have the same name, regardless of AWS account or region. This is because the bucket name is part of the bucket’s URL and is used to uniquely identify it across all of Amazon S3.

![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this stop, we are going to doanload an HTML file that sets up the website. Moreover, we are also going to download the images that the website will utilize. 

The most important step of this phase is to upload the aforementioned files in the S3 bucket. 

### Files I uploaded

I upload two files in my S3 bucket. First is the HTML file and second is the folder that contains the resources that will be used by the static website. 

### How the files work together

Both files are necessary to this project since the HTML only contains the structure of the website. Additional resources are needed for the design ang behavior of the whole website. 

![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will configure the S3 bucket for static website hosting and visit the public website link to determine if the website is properly launched and to check for the missing resources if ever. 

### Understanding website hosting

Website hosting means storing your website's files (HTML, CSS, images, code, etc.) on a server that's connected to the internet, so other people can access it via a browser.

Think of it like renting space on a computer that's always online. When someone types your domaininto their browser, their request is routed to that server, which serves back your website's content.

### How I enabled website hosting

To enable a website hosting in Amazon S3, I edited the properties of my bucket to make static web hosting possible. It can be done by enablic static website hosting, choosing hosting type, and entering the html document. 

### Access Control Lists (ACLs)

In this project, I enabled Access Control List (ACL). It means that objects in this AWS account can be owned by other AWS accounts. 

![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

A bucket website endpoint URL is the web address that S3 gives you when you enable static website hosting on a bucket. It's how visitors access your site hosted on S3.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw an error message stating "403 Forbidden". It means that the server understood my request but refuses to fulfill it since I don't have permission to access that resource.

I saw this message since objects in S3 bucket are private by default. This helps maintaining a more secured bucket. 


![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will make the website files in the S3 bucket more publicly accessible.

### How I resolved the 403 error

To resolve the 403 Forbidden error, I made my resources public using ACLs. 

![Image](http://nextwork.ai/joyful_orange_bold_kaki/uploads/aws-host-a-website-on-s3_5d4474f9)

---

