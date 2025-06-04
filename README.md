# ☁️ Cloud Resume Challenge (Backend + Frontend) – AWS Edition

This project is part of the [Cloud Resume Challenge](https://cloudresumechallenge.dev/) — a hands-on initiative designed to reinforce practical cloud skills. This repository documents my implementation of the backend and frontend components of the challenge, including a live visitor counter connected to my personal resume site.

---

## 🧠 Objectives

- Build and deploy a cloud-native resume
- Use AWS services to build a **serverless visitor counter**
- Connect backend API to frontend JavaScript
- Deploy the static site using S3 + CloudFront + custom domain
- Strengthen security and scalability practices

---

## 🔧 Tech Stack

- **AWS Lambda** – Python function to update visitor count
- **Amazon DynamoDB** – NoSQL database to store visit count
- **API Gateway (REST API)** – Exposes Lambda as a RESTful API
- **IAM Roles & Policies** – Secure access between services
- **Amazon CloudWatch** – Logs for Lambda execution
- **JavaScript + HTML** – Frontend to fetch/display visitor count
- **Amazon S3** – Static website hosting for the resume
- **CloudFront** – CDN for performance and reliability
- **Custom Domain + SSL (AWS ACM)** – Secure, professional branding
- **Terraform (optional)** – Infrastructure as Code (planned)

---

## ✅ Completed Steps

### 🔹 Backend:
- Created a DynamoDB table with `visitor_count` item
- Wrote a Python Lambda function to get/increment the counter
- Deployed function using the AWS Console
- Created a REST API Gateway with CORS enabled
- Integrated the API with the Lambda function using stage `prod`
- Configured IAM permissions so API Gateway can invoke Lambda
- Verified response with Postman and browser

### 🔹 Frontend:
- Simple HTML page with embedded JavaScript
- JS fetches data from the deployed REST API endpoint
- Displays current visitor count inside a `<span>` element
- Deployed the website to **Amazon S3**
- Configured **CloudFront** distribution for global CDN performance
- Connected a **custom domain** with **SSL certificate (ACM)** for secure, trusted hosting

---

## 🔐 Security & IAM
- Created a least-privilege IAM role for Lambda with:
  - `dynamodb:GetItem`, `dynamodb:UpdateItem`
- Added API Gateway invocation permission on Lambda:
  - `lambda:InvokeFunction` from `apigateway.amazonaws.com`

---

## 📈 Skills Gained

- ✅ Real-world AWS service integration
- ✅ Serverless application development
- ✅ IAM permission modeling & security best practices
- ✅ REST API Gateway setup (latest 2025 AWS Console UI)
- ✅ Debugging CORS and testing REST APIs
- ✅ JavaScript API consumption from a secured backend
- ✅ Logging with CloudWatch
- ✅ Hosting static websites with S3 and CloudFront
- ✅ Domain management and HTTPS (SSL/TLS) with AWS ACM

---

## 🚀 Live Demo

> 🔗 https://ken-joiner.com/
> Try it! Refresh the page and watch the visitor counter increase!

---

## 📝 Next Steps

- [ ] CI/CD with GitHub Actions for automated deployments
- [ ] Infrastructure as Code with Terraform for reproducible environments
- [ ] Enhanced security and performance best practices

---

## 📸 Screenshot
![visitcounter](https://github.com/user-attachments/assets/bd8b9b92-6801-47b0-aaa2-62774ca90c41)

---

## 📚 License

This project is licensed under the MIT License.
