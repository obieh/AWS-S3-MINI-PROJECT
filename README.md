# AWS-S3-MINI-PROJECT.
## This Project demonstrates S3 concepts in AWS.

#### Amazon S3 bucket is a public cloud storage resource available in Amazon Web Services (AWS) Simple Storage Service (S3) platform. It provides object-based storage, where data is stored inside S3 buckets in distinct units called objects instead of files.

![](./img/Pasted%20image.png)


#### Uses of S3 Bucket:Any type of data can be stored using it – although it may not suit some application use cases, such as databases – and these can include documents, video and images. Objects are stored with a unique identifier. This is what distinguishes object storage from traditional file and block. 

### Common use cases.
* Backup and archival
* Big Data Analytics
* Websites files and folders
* File delivery fast.

### S3 core concepts:

![](./img/Pasted%20image%20(2).png)

* Buckets: are cognitive equivalent to folder where you store files.

* Object: Files that you can store in the bucket.
* Keys: Unique identifiers for the objects stored in a bucket.
* Storsge Classes.
  1. S3 Standard
   2. S3 Standard-IA
   3. S3 Intelligent-Tiering
  4. S3 One Zone-IA
  5. S3 Glacier
  6. S3 Glacier Deep Archive
  7. S3 Outposts

* Acess Control: Access Control Lists(ACLs) Identity Acess Manager(IAM)and Bucket Ploicies can be used to control access.

* Durability and Availability: S3 is built for high availability and durability. There is almost 0 chance of data loss.

* Data Transfer: S3 support inbound and outbound file transfers. RFile trnafers can be done via AWS console, AWS cli, SDK and third party tools.

* Versioning: S3 support a category storage option called versioning. This feature protects against accidental delete of files. It can also store different version of a file.

## Creation os Amazon S3 Bucket.

* Head over to your AWS account. Type S3 in the search bar and click 'S3'.

![](./img/Pasted%20image%20(3).png)

* Click 'Create bucket'

![](./img/Pasted%20image%20(4).png)

* Choose a name for the bucket. Disable ACL.

![](./img/Pasted%20image%20(5).png)


* Select 'Block all public access' option. Ensure Bucket versioning is disabled.

![](./img/Pasted%20image%20(6).png)

* Leave encryption at 'server-side'. Bucket Key 'Enabled' and click 'create bucket'.

![](./img/Pasted%20image%20(7).png)

* Success page should popup, indicating bucket was successfully created.

![](./img/Pasted%20image%20(8).png)

## Uploading Content.
* Create a simple text file or any file of your choice.

![](./img/Pasted%20image%20(9).png)

* Click on the S3 bucket you just created and click upload.

![](./img/Pasted%20image%20(10).png)

* Click 'Add files' to begin adding files to your S3 bucket.

![](./img/Pasted%20image%20(11).png)

* Navigate to the location of rhe file you want to add, select the file then click upload.

![](./img/Pasted%20image%20(12).png)

* If file upload is successful, you should see a confirmation page.

![](./img/Pasted%20image%20(13).png)



### Enable Versioning on S3 Bucket.

* Click on the S3 bucket name and select the properties tab.

![](./img/Pasted%20image%20(14).png)

* On the Bucket Versioning block click 'edit', Select 'enable' and click 'Save changes'

![](./img/Pasted%20image%20(15).png)

* A success page shows up implying versionin has been enabled.

![](./img/Pasted%20image%20(17).png)

* Add some more content to the local file uploaded earlier.

![](./img/Pasted%20image%20(16).png)

* Upload the new version of the file to your bucket.

On the S3 bucket toggle the show version knob to see the version of the file.

![](./img/Pasted%20image%20(18).png)

### Setting/Editing Permisions.

* On the S3 bucket select permisions tab.

![](./img/Pasted%20image%20(19).png)

* Move a bit down to 'Block public access (bucket settings)' and click 'edit'.

![](./img/Pasted%20image%20(20).png)

* Uncheck 'Block all public access' and click to save the changes.

![](./img/Pasted%20image%20(21).png)

* Type 'confirm' and click confirm to save changes.

![](./img/Pasted%20image%20(22).png)

* We just removed 'Block all public access' policy from our S3 bucket A success page should confirm this.

![](./img/Pasted%20image%20(23).png)


### Create Policy

* Move down to "Bucket Ploicy" and click edit.

![](./img/Pasted%20image%20(24).png)

* Towards the right click 'Policy Generator'.

![](./img/Pasted%20image%20(25).png)

* Select 'S3 Bucket Policy' in policy type drop down.
* Set the 'Effect' to 'Allow'.
* Specify the 'Principle' as "*", signifying all users.
* Choose the action "Get object"  and "Get Object version".
* Type the Amazon Resource Name(ARN) of your bucket and suffix with "/*" in the ARN field.
* Click 'Add statement'.

![](./img/Pasted%20image%20(26).png)

* Verify you have added "GetObjectVersion" and "GetObject" and click "Generate Policy".

![](./img/Pasted%20image%20(28).png)

* Copy the Policy and close the pop up window.

![](./img/Pasted%20image%20(29).png)

* Got back to the previous window, paste the copied policy and click 'save changes'.

![](./img/Pasted%20image%20(29).png)

* You should see a sucess page 'Successfully edited bucket policy'.

![](./img/Pasted%20image%20(30).png)

* Head over to the first version of your file in the S3 bucket.

![](./img/Pasted%20image%20(31).png)

* copy the object Uniform Resource Locator and head over to your browser. Past and hit enter.

![](./img/Pasted%20image%20(32).png)

* Now our file is now available and can be accessed publicly. Do same for the second version.

![](./img/Pasted%20image%20(33).png)

* Indeed the second version can also be accessed publicly.

### Creating Lifecycle policies.

* Click the Managment tab of the S3 bucket.

![](./img/Pasted%20image%20(34).png)

* On the lifecycle section click 'create lifecycle rule'.

![](./img/Pasted%20image%20(35).png)

* Add a name for the lifecycle rule. Select "Limit the scope of this rule using one or more filters" for Choose a rule scope. On the filter prefix type '.txt'.

![](./img/Pasted%20image%20(36).png)

* Set object size to 2gb. Set maximum object size to 10gb. Check "Transition current versions of objects between storage classes, check to acknowledge that the rule will incur cost per request". Set 'Choose Storage class transition' to 'Standard -IA' and 'Days after object creation' to '30', Then click creat rule.

![](./img/Pasted%20image%20(37).png)

* You should a success page indicating lifecycle rule was successfully aadded.

![](./img/Pasted%20image%20(38).png)


