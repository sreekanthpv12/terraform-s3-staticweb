# terraform-s3-staticweb


# Setting Up an AWS S3 Bucket with Terraform

This repository provides a step-by-step guide on setting up an AWS S3 bucket using Terraform. The guide covers various aspects of creating and configuring an S3 bucket for static website hosting.

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) installed
- AWS access key and secret key configured

## Steps

1. Create `provider.tf`:
   - Copy the AWS provider configuration from the HashiCorp documentation.
   - Run `terraform init` to initialize the AWS provider.

2. Create `main.tf`:
   - Define the S3 bucket resource.
   - Utilize variables defined in `variable.tf`.

3. Create `variable.tf`:
   - Define variables for customization.
   - Reference these variables in `main.tf`.

4. Define Bucket Ownership:
   - Use `aws_s3_bucket_ownership_controls` to specify ownership.

5. Configure Public Access:
   - Utilize `aws_s3_bucket_public_access_block` to manage public access.

6. Create `aws_s3_bucket_acl`:
   - Set up a public-read ACL for the S3 bucket.

7. Enable Static Website Hosting:
   - Define the static website configuration using `aws_s3_bucket_website_configuration`.

8. Upload Objects:
   - Upload `index.html`, `error.html`, and `profile.png` objects to the S3 bucket using `aws_s3_object`.

9. Configure Website Hosting:
   - After uploading objects, configure the website hosting using `aws_s3_bucket_website_configuration`.

10. Access the Website:
    - Go to AWS S3 properties, find the website hosting URL, and access the application.

11. Embed Profile Image:
    - In `index.html`, use the URL of `profile.png` to display the profile image.

## Usage

1. Clone this repository.
2. Follow the step-by-step guide in each file.
3. Customize variable values in `variable.tf` as needed.
4. Run `terraform init`, `terraform plan`, and `terraform apply` for each step.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
