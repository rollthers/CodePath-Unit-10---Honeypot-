# Honeypot Assignment

**Time spent:** **X** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

In order to have a space to deploy the honeypot, I would need to boot up some cloudspace. I made use of GCP's free trial to host my honey pot. The set up of my cloud was seamless, and initalizing it took place during the installation. After it's install, I set the time zone to US centeral, and checked to ensure my configs were correctly set up by using `gcloud config list`. 

![GCloud proof](https://user-images.githubusercontent.com/95894083/167200040-f8aa91b6-cee4-46e2-9126-29bd717585c6.gif)

Once I set up the GCP server, I moved towards integrating the MHN VM. To start this, I referenced the code provided on the assignment doc to configure my firewalls for GCP to the following: 

![image](https://user-images.githubusercontent.com/95894083/167202372-d599f8f6-fbbc-4174-9a96-afc0897f1332.png)



### Dionaea Honeypot Deployment (Required)

**Summary:** Briefly in your own words, what does dionaea do?

<img src="dionaea-honeypot.gif">

### Database Backup (Required) 

**Summary:** What is the RDBMS that MHN-Admin uses? What information does the exported JSON file record?

*Be sure to upload session.json directly to this GitHub repo/branch in order to get full credit.*


## Notes

The assignment was pretty easy to follow; however, it was annoying to realize that I forgot to document my own steps. Therefore, I had to go back and redo it again. 
