🌟 Steps for Setting Up and Deploying the MERN App on AWS
1️⃣ Set Up EC2 (Backend):

Launched a t3.micro instance in eu-north-1 with Ubuntu 22.04 LTS.

Configured Security Groups to allow access on the following ports:

SSH: 22

HTTP: 80

HTTPS: 443

Custom TCP: 5000

Used a User Data Script to install necessary tools like Node.js, AWS CLI, MongoDB Shell, and PM2.

Deployed the backend using PM2.

2️⃣ Set Up Frontend (React):

Created an S3 Bucket to upload React files.

Enabled Static Website Hosting for the S3 bucket.

Uploaded the React build to the S3 bucket using aws s3 sync.

3️⃣ Set Up S3 for Media (Uploads):

Created a new S3 Bucket for uploading media files (e.g., images, videos).

Configured CORS for browser upload support.

Tested uploading and retrieving files from AWS S3.

4️⃣ Create IAM User:

Created a new IAM User with permissions to access the S3 Bucket.

Generated Access Key ID and Secret Access Key for the IAM user and used them in the configuration files.

5️⃣ Configure Environment Variables:

Created a .env file for both backend and frontend with the following details:

MongoDB connection string.

AWS Access Keys.

S3 Bucket names.

JWT Authentication keys.

6️⃣ Deploy Backend:

Installed dependencies using npm and set up the backend to run on port 5000.

Started the server using PM2 and set it to start on system reboot.

7️⃣ Deploy Frontend:

Installed dependencies using pnpm and built the React app.

Deployed the build files to S3 using AWS CLI.

8️⃣ Verification:

Verified that the backend is running via PM2.

Verified that the frontend is correctly hosted on S3.

Ensured media files were uploaded successfully to S3.
