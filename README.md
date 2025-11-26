# AWS S3 OBJECT STORAGE OPERATIONS USING AWS CLI (FROM LOCAL MACHINE)

This repository contains all steps and AWS CLI commands demonstrated in
the YouTube tutorial on how to work with Amazon S3 from your local
machine.

### 📺 YouTube Tutorial

https://youtu.be/nslQDVhsvHI

------------------------------------------------------------------------

## 📌 OVERVIEW

This project covers the following:

-   Installing AWS CLI\
-   Configuring AWS credentials\
-   Creating an S3 bucket\
-   Uploading files and folders to S3\
-   Downloading files from S3\
-   Listing buckets and objects\
-   Syncing folders\
-   Deleting objects and buckets

------------------------------------------------------------------------

## 🧰 REQUIREMENTS

Before running the commands, ensure:

1.  You have an AWS account\
2.  AWS CLI is installed\
3.  IAM user has S3 permissions\
4.  AWS CLI is configured using the command:

``` bash
aws configure
```

------------------------------------------------------------------------

## 🚀 AWS CLI COMMANDS USED IN THE TUTORIAL

### 1️⃣ Check AWS CLI Installation

``` bash
aws --version
```

### 2️⃣ Configure AWS Credentials

``` bash
aws configure
```

### 3️⃣ Create an S3 Bucket

``` bash
aws s3 mb s3://your-bucket-name
```

### 4️⃣ List All Buckets

``` bash
aws s3 ls
```

### 5️⃣ Upload a File to S3

``` bash
aws s3 cp file.txt s3://your-bucket-name/
```

### 6️⃣ Upload a Folder to S3

``` bash
aws s3 cp myfolder s3://your-bucket-name/ --recursive
```

### 7️⃣ List Objects in a Bucket

``` bash
aws s3 ls s3://your-bucket-name/
```

### 8️⃣ Download a File from S3

``` bash
aws s3 cp s3://your-bucket-name/file.txt .
```

### 9️⃣ Sync a Local Folder with S3

``` bash
aws s3 sync myfolder s3://your-bucket-name/
```

### 🔟 Delete an Object

``` bash
aws s3 rm s3://your-bucket-name/file.txt
```

### 🧹 Delete an S3 Bucket

``` bash
aws s3 rb s3://your-bucket-name --force
```

------------------------------------------------------------------------

## 📂 REPOSITORY STRUCTURE

    README.md
    files/
        example.txt
        sample-folder/

------------------------------------------------------------------------

## 📝 NOTES

-   S3 bucket names must be globally unique\
-   Be careful with delete commands, especially the `--force` option\
-   Use IAM users instead of root credentials\
-   `sync` is useful for fast and automatic uploads

------------------------------------------------------------------------

## 📄 LICENSE

This project is open-source and free to use.
