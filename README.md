#  Laravel 5 Beanstalk Template
> Piethein Strengholt (2017)

## About
An example template for deploying Laravel applications with AWS Beanstalk.

## Explanation
Just copy and paste the files from this repository to your Laravel project. Beanstalk uses a zip file for the final deployment, so you need to add your .env file to the final package as well. The .env file should have the APP_KEY properly set.

## 01init.config script
The 01init.config script takes care of the after deployment steps, such as the composer update and artisian migration. The script also sets the public folder and increases the PHP memory limit to 512MB.

## AWS variables
It is very much recommended to a RDS database. When doing so, add the database.php from the config folder to Laravel's config folder. The AWS RDS variables are passed to the EC2 server, so no additional tuning is needed. Make sure the DB_HOST, DB_DATABASE, DB_USERNAME and DB_PASSWORD are set to empty in the .env file.
