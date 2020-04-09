1. Setting up a cloud solution environment  

    1.1 Setting up cloud projects and accounts. Activities include:      
    - Creating projects  
    - Assigning users to predefined IAM roles within a project  
    - Managing users in Cloud Identity (manually and automated)
    - Enabling APIs within projects
    - Provisioning one or more Stackdriver workspaces  

    1.2 Managing billing configuration. Activities include:  
    - Creating one or more billing accounts
    - Linking projects to a billing account
    - Establishing billing budgets and alerts
    - Setting up billing exports to estimate daily/monthly charges  

    1.3 Installing and configuring the command line interface (CLI), specifically the Cloud SDK (e.g., setting the default project).

--------------------


Run  `gcloud compute instances create --help` to see all the defaults.

Note: You can set the default region and zones that gcloud uses if you are always working within one region/zone and you don't want to append the --zone flag every time. Do this by running these commands :

```
gcloud config set compute/zone ...

gcloud config set compute/region ...
```
To see what your default region and zone settings are  
`gcloud compute project-info describe --project <your_project_ID>`


Setting environment variables  
```
export PROJECT_ID=<your_project_ID>
export ZONE=<your_zone>

echo $PROJECT_ID
echo $ZONE
```

creating a virtual machine with GCloud  

`gcloud compute instances create gcelab2 --machine-type n1-standard-2 --zone $ZONE`

You can see the default values by displaying help for the create command:
`gcloud compute instances create --help`

you can SSH into your instance using gcloud as well. Make sure you add your zone, or omit the --zone flag if you've set the option globally:

`gcloud compute ssh gcelab2 --zone [YOUR_ZONE]`
