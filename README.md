# Honeypot Assignment

**Time spent:** **5** hours spent in total

**Objective:** Create a honeynet using MHN-Admin. Present your findings as if you were requested to give a brief report of the current state of Internet security. Assume that your audience is a current employer who is questioning why the company should allocate anymore resources to the IT security team.

### MHN-Admin Deployment (Required)

In order to have a space to deploy the honeypot, I would need to boot up some cloudspace. I made use of GCP's free trial to host my honey pot. The set up of my cloud was seamless, and initalizing it took place during the installation. After it's install, I set the time zone to US centeral, and checked to ensure my configs were correctly set up by using `gcloud config list`. 

![GCloud proof](https://user-images.githubusercontent.com/95894083/167200040-f8aa91b6-cee4-46e2-9126-29bd717585c6.gif)

Once I set up the GCP server, I moved towards integrating the MHN VM. To start this, I referenced the code provided on the assignment doc to configure my firewalls for GCP to the following: 

![image](https://user-images.githubusercontent.com/95894083/167202372-d599f8f6-fbbc-4174-9a96-afc0897f1332.png)

After setting this firewall up, I took to downloading and patching the required script for MHN, via cloning `https://github.com/pwnlandia/mhn.git` in my admin VM.

### Dionaea Honeypot Deployment (Required)

Dionaea is a honeypot that uses python script and libemu to detect shell-codes and scans of a server. When a scan is conducted on the honeypot, the Src IP, time, country (at least where they have set their contry to be), and port attacked are recorded. Additonally, a protocol is displayed for each scan. To deploy the honeypot, I inserted the deploy command into the MHN VM to create a sensor that utilized the script. 


![DionaeaIntegrate](https://user-images.githubusercontent.com/95894083/167226325-11b91b19-af8b-4d0f-805d-5213ecd6b799.gif)

Unfortunately, due to already running this honeypot, I was not able to show it being created. If all goes well, the sensor should now be visible under the "sensors" tab in our MHN Server website. Using our IP to access the the website, the finish product looks like the following. 

![image](https://user-images.githubusercontent.com/95894083/167228095-72fd7c79-b747-4db8-8590-048cdc788374.png)

### Database Backup (Required) 

To be able to export our results as a downloadable .json file, I utilized mongo export in the admin VM, and packed the size to less than five megabytes to avoid uploading issues. The command to export our results is shown below. 

![mongoexport](https://user-images.githubusercontent.com/95894083/167230204-ec22f1ed-65ad-426e-b838-93c0be2fb84a.gif)

## Notes

The assignment was pretty easy to follow; however, it was annoying to realize that I forgot to document my own steps. Therefore, I had to go back and redo it again. 
