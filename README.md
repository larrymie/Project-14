# Project-14
**EXPERIENCE CONTINUOUS INTEGRATION WITH JENKINS | ANSIBLE | ARTIFACTORY | SONARQUBE | PHP

I deployed a Redhat webserver on aws ec2  instance and named it jenkins-ansible. downloaded jenkins and its dependencies on the jenkins-ansible server.
Java was first installed and saved as documented in the README.md ansible-config repo cloned. followed by the actual installation of of jenkins. **IMAGES 1
![01](https://user-images.githubusercontent.com/91284177/155186514-17e9f6d0-8df3-492a-b440-f5f21361bfa3.png)

Jenkins was succeessfully installed and active as shown in **IMAGE 02
![02](https://user-images.githubusercontent.com/91284177/155187537-157beeb3-0014-4dcf-8883-5d9fed50492f.png)

**Configured Ansible For Jenkins Deployment

Navigated to Jenkins URL, Installed & Opened Blue Ocean Jenkins Plugin and also created a new pipeline **IMAGES 03-08
![03](https://user-images.githubusercontent.com/91284177/155356232-ed16f53a-440f-4d8e-9f8e-0d40cc1f4421.png)
![04](https://user-images.githubusercontent.com/91284177/155356259-b68f96e4-fca7-4788-8ca7-5a13d370cd45.png)
![05](https://user-images.githubusercontent.com/91284177/155356280-59a255b9-e9f7-484f-adfc-7eff49fc2951.png)
![06](https://user-images.githubusercontent.com/91284177/155356491-151d6433-99e3-44f8-bfa0-0bc945b61b7b.png)
![07](https://user-images.githubusercontent.com/91284177/155356638-f4415265-7e62-4c63-91df-7265172e8c36.png)
![08](https://user-images.githubusercontent.com/91284177/155356654-e43fc91c-63cb-40c6-b695-9ee77994fb60.png)

Then clicked on administration to exit the blue ocean console. **IMAGE 09
![09](https://user-images.githubusercontent.com/91284177/155357620-960326bc-44bb-483f-ab5d-1cef115f99bf.png)

Inside the Ansible project, I created a new directory deploy and start a new file Jenkinsfile inside the directory. **IMAGE 10
![10](https://user-images.githubusercontent.com/91284177/155357807-4ab12239-d370-4564-ac48-dc666cc7d12b.png)
![10](https://user-images.githubusercontent.com/91284177/155357817-fc3258a5-b415-4536-96bb-494fcf131556.png)

Added the code snippet below to start building the Jenkinsfile gradually. **IMAGE 11

![11](https://user-images.githubusercontent.com/91284177/155358230-8cb74930-54a0-44f5-8f80-1a351cae35e6.png)

Added deploy to the path of jenkinsfile in the jenkins build. **IMAGE 12
![12](https://user-images.githubusercontent.com/91284177/155358509-a525620d-5485-4a0c-a0d9-38bf9d84c789.png)

In Blue Ocean, i saw how the Jenkinsfile has caused a new step in the pipeline launch build for the first branch. **IMAGE 13
![13](https://user-images.githubusercontent.com/91284177/155359055-9904edcb-c524-4cdd-9b0c-0393dcd9125b.png)

Another stage was added to the jenkinsfile which is 'test' **IMAGE 14
![14](https://user-images.githubusercontent.com/91284177/155359464-f82b57bd-0c95-4f89-8879-87fd04d77d97.png)

Scanned ansible-config-mgt repo to successfully buit the testing stage. **IMAGE 15
![15](https://user-images.githubusercontent.com/91284177/155360030-f8b0ce03-b7af-484e-b715-bf7e80ab5fe5.png)

In Blue Ocean, i could see how the Jenkinsfile has caused a new step in the pipeline launch build for the new branch. **IMAGE 16
![16](https://user-images.githubusercontent.com/91284177/155360406-d56f5f63-5560-456e-a345-6edbcda55ecb.png)

I Created a pull request to merged the latest code into the main branch. with the result showing success. **IMAGE 17
![17](https://user-images.githubusercontent.com/91284177/155360995-4ce9cadb-f857-4b6a-8299-a07ae115abae.png)













