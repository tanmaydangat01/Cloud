### Step-by-Step Guide for Configuring S3 Object Encryption with AWS KMS

---

### Step 1: Create an S3 Bucket

1. **Open the S3 Service**:
   - Navigate to the **S3** service in the AWS Management Console.

2. **Create a New Bucket**:
   - Click on **Create bucket**.
   - Enter a unique name for your bucket and configure other settings as needed.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS1.png)
)
   
3. **Finalize Bucket Creation**:
   - Scroll down and click **Create bucket**.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS1.png)

---

### Step 2: Enable Default Encryption for the S3 Bucket

1. **Open the Created Bucket**:
   - In the S3 dashboard, click on the name of the bucket you just created.

2. **Navigate to the Properties Tab**:
   - Go to the **Properties** tab in the bucket settings.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS2.png)

3. **Edit the Default Encryption Settings**:
   - Scroll to the **Default encryption** section and click **Edit**.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS3.png)

4. **Select AWS Key Management Service (KMS)**:
   - Under **Server-side encryption settings**, select **AWS Key Management Service keys (SSE-KMS)**.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS4.png)

5. **Choose AWS Managed Key (aws/s3)**:
   - For encryption, select **AWS managed key** (default option) if you don’t want to use a custom key.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS5.png)

6. **Save Changes**:
   - Click **Save changes** to apply the encryption settings.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS5.png)

---

### Step 3: Upload and Verify Encryption

1. **Upload a File to the Encrypted Bucket**:
   - In your bucket, go to the **Objects** tab and click **Upload**.
   - Select a file from your local system to upload to the bucket and complete the upload process.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS6.png)

2. **Verify Encryption Status**:
   - After uploading, click on the file name to view its **Properties**.
   - In the **Server-side encryption settings**, confirm that **AWS-KMS** encryption is applied with **aws/s3** as the key.
   ![S3 Bucket Creation](IAM%20S3%20Object%20Encryption%20with%20AWS%20KMS/KNS7.png)
