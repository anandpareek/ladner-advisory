# Ladner Advisory — Website

A three-page static website for Ladner Advisory.

## Project Structure

```
ladner-advisory/
├── index.html       # Home page
├── about.html       # About page (Dr. Thomas Ladner bio)
├── contact.html     # Contact page with enquiry form
├── assets/
│   ├── Logo_Smita.png     # Ladner Advisory logo
│   └── Dr. Thomas Ladner.png  # Dr. Ladner portrait
└── README.md
```

## Features

- **Responsive Design**: Clean, modern dark theme with white accents
- - **Three-Page Site**: Home, About (with Dr. Ladner bio & career timeline), Contact
  - - **Professional Look**: Inspired by parent company e-r-t.org design language
    - - **Contact Form**: Ready-to-integrate form with subject dropdown
      - - **Assets Included**: Logo and Dr. Ladner's professional portrait
       
        - ## Setup
       
        - 1. All logo and image assets are already in `assets/` folder
          2. 2. **Update contact details**: In `contact.html`, replace the placeholder phone number and email
             3. 3. **Connect the contact form**: The form currently shows a success message. To make it functional, integrate:
                4.    - [Formspree](https://formspree.io) (easiest, no backend needed)
                      -    - AWS SES + API Gateway (serverless)
                           -    - Any backend of your choice
                            
                                - ## Deploying to AWS
                            
                                - ### Option 1 — S3 Static Website Hosting
                                - 1. Create an S3 bucket named e.g. `ladner-advisory.com`
                                  2. 2. Enable **Static website hosting** in Bucket settings
                                     3. 3. Upload all files maintaining the folder structure
                                        4. 4. Set a bucket policy for public read access
                                           5. 5. Access via the S3 website endpoint
                                             
                                              6. ### Option 2 — S3 + CloudFront (Recommended for custom domain + HTTPS)
                                              7. 1. Set up S3 as above
                                                 2. 2. Create a **CloudFront distribution** pointing to the S3 bucket
                                                    3. 3. Add your custom domain in CloudFront settings
                                                       4. 4. Request an SSL certificate via **AWS Certificate Manager (ACM)**
                                                          5. 5. Update your DNS records to point to the CloudFront distribution
                                                            
                                                             6. ### Option 3 — AWS Amplify (Easiest full setup)
                                                             7. 1. Go to [AWS Amplify Console](https://console.aws.amazon.com/amplify/)
                                                                2. 2. Connect your GitHub repository
                                                                   3. 3. Amplify will auto-deploy on every push to `main`
                                                                      4. 4. Add a custom domain in Amplify settings
                                                                        
                                                                         5. ---
                                                                        
                                                                         6. *Built for Smita — April 2026*
                                                                         7. *Project: ladner-advisory | Owner: anandpareek*
