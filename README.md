# final-project-cloud-computing-foundations
This is the final project for Duke's course Cloud Computing Foundations hosted on Coursera's platform.

The objective of the project is to build a Hugo Static Website that is continuously deployed using AWS Code Build and AWS S3 Static Hosting.

I will describe here the steps followed to construct the entire project.
## Steps:
1. Setup a Cloud9 working environment
2. Download the latest version of Hugo from Hugo's Git repository
3. Generated Hugo website with quickstart
  - Gen .gitignore to ignore public files when executing
4. Get a theme from Hugo themes and connected it to my repo
5. Changed my instance's security groups to allow public access to port 8080
6. Started running it with Hugo
7. Command "hugo" in terminal to create public dir
8. Deploy it on S3 so it can be available
	- Properties -> Static Website hosting
	- Change access
	- Save files from public folder to S3 objects

## Continuous Delivery
Now all this steps we can be made automatically with AWS CodeBuild, and it prevents you from making mistakes in the process. It will
do this automatically everytime I push something into my Git repo.

All the steps were described in this [site](https://paiml.com/docs/home/books/cloud-computing-for-data/chapter02-cloud-foundations/#continuous-delivery-for-hugo-static-site-from-zero)

1. Configurate AWS CodeBuild
	- Source will be my github repo
	- Needed to create a token on git (as explained [here](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)).

**Observation**
I had some issues on the way, cause I didn't have administrator permitions allowed in my CodeBuild, so I tried some different solutions before getting it right. This is a image of how it looked like when I finaly solved it.

![image](https://github.com/giovana-claro/final-project-cloud-computing-foundations/assets/139156735/809341a1-a508-41a9-a82e-24cd172fa5a9)

**Conclusion**
This was a really cool project to gather everything I learned and put this in practice, cause there is when you really understand the details of the process, correcting errors and making it work.
I realised how important DevOps practices are and how it can automate process, avoiding errors and speeding up the deployment and traking of errors through Continuous Delivery pipelines.  
