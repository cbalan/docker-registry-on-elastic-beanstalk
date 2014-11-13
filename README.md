## Quick Setup

 * clone the repository
 * zip it ```zip -r docker-registry.zip .ebextensions Dockerrun.aws.json```
 * set up an S3 bucket and a IAM role to access it
 * create a new app and environment in elastic beanstalk to run a Docker WebServer
 * when the wizard asks you set the following environment variables:
  * ```AWS_BUCKET``` name of the bucket
  * ```SECRET_KEY``` optional - a random secret key, the registry uses this for secret things (https://github.com/dotcloud/docker-registry#general-options)
 * when the wizard asks you for the app, upload the zip file
 * complete the wizard
 * wait for the environment and app to spin up
 * profit

the registry will be running on port 80 (not 5000)
