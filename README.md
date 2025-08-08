# AWS-S3-MINI-PROJECT.
## This Project demonsts S3 conepts in AWS.

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

## Creation os Amazon S3 Bucket

* Head over to your AWS account. Type S3 in the search bar and click 'S3'

![](./img/Pasted%20image%20(3).png)

* Click 'Create bucket'

![](./img/Pasted%20image%20(4).png)

* Choose a name for the bucket. Disable ACL.

![](./img/Pasted%20image%20(5).png)


