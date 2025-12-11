
# 🚀 Static Website Hosting on AWS S3

This repository contains a simple static website hosted on **Amazon S3**.  
AWS S3 provides an easy and cost-effective way to host static content such as HTML, CSS, JavaScript, and images.

---

## 📚 Steps to Host a Static Website on AWS S3

### **1. AWS S3**
Amazon S3 (Simple Storage Service) is used as the hosting platform to store the website files.

---

### **2. Simple Static Website**
The project includes basic static files such as:
- `index.html`
- CSS stylesheets
- Images
- Optional JavaScript files

---

### **3. Create an S3 Bucket**
1. Go to the **AWS S3 Console**
2. Click **Create bucket**
3. Enter a unique bucket name
4. Select your AWS region
5. Disable **Block all public access**
6. Create the bucket

---

### **4. Upload Files**
1. Open your S3 bucket
2. Go to the **Objects** tab
3. Click **Upload**
4. Add your website files
5. Click **Upload** to save them in S3

---

### **5. Configure Static Website Hosting**
1. Open your bucket → go to the **Properties** tab
2. Scroll to **Static website hosting**
3. Click **Edit**
4. Enable static hosting
5. Choose **Host a static website**
6. Set:
   - **Index document:** `index.html`
   - **Error document:** (optional)
7. Save changes

---

### **6. Set Permissions**
To allow the website to be publicly accessible:

1. Go to **Permissions** → **Bucket Policy**
2. Add this policy (replace `your-bucket-name`):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
````

3. Save the policy

---

## 🌍 Website Access

After completing all steps, your static website will be available via the S3 **Website Endpoint URL**, found under the **Static website hosting** section.

---


