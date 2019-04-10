# Code Pipeline
This section is used to push the github cloudformation files into an S3 bucket.  
As Cloudformation does not allow the use of templates from github directly we need to add them into an S3 bucket.  
### Cloudformation template
The CF template in here creates the pipeline, S3 bucket and appropriate permissions for use.  
This pipeline has a hook into Github that detects changes within the repo and initiates the pipeline.  
In turn the pipeline pushes the code from github into a build phase initating the buildspec file (also in this directory). 
The buildspec simply copies the contents of the /Cloudformation directory to a bucket and makes the files public.  
SSM Parameters are used to store/read values such as GitHub secrets and allow their re-use.
### Why?
The pipeline removes a manual step of copying files into the S3 bucket and, effectively, keeps the S3 bucket in sync with the Github repo.