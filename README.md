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

I Created a pull request to merge the latest code into the main branch. with the result showing success. **IMAGE 17
![17](https://user-images.githubusercontent.com/91284177/155360995-4ce9cadb-f857-4b6a-8299-a07ae115abae.png)

The jenkins file was successfully runned. as shown in the jenkins blue ocean pipeline **IMAGE 18 
![18](https://user-images.githubusercontent.com/91284177/156926541-5139221f-7d7c-4bc5-a32f-dbee5cc3147b.png)

I downloaded ansible on jenkins server and also downloaded it on jenkins user interface as a plugin. **IMAGES 19 and 20
![19](https://user-images.githubusercontent.com/91284177/156926628-09caf2de-502e-4cdc-be45-4ee9d4f582ae.png)
![20](https://user-images.githubusercontent.com/91284177/156926761-76a992f6-2d34-4e70-981c-fc8c72e49bba.png)

Remember jenkins was written in python language, this necessitate installing some dependencies for jenkins to successfully run jenkins file. **IMAGE 21
![21](https://user-images.githubusercontent.com/91284177/156926848-68841a86-3dbf-4942-b135-841f5d081d67.png)

I added the pem key of the jenkins server to jenkins ansible to enable it to talk to DB server and NGINX server accordingly. **IMAGE 22 
![22](https://user-images.githubusercontent.com/91284177/156926930-c2da49e8-434c-4cea-85b3-d0184ee96faf.png)

The pipeline was successfully runned with a particular attention to ansible playbook. **IMAGES 23 & 24
![23](https://user-images.githubusercontent.com/91284177/156927032-83145d3b-f949-4624-8e3a-ae28e199baab.png)
![24](https://user-images.githubusercontent.com/91284177/156927026-2a283fef-9cae-442c-a2b0-5cccd923e97c.png)

for jenkins to run files from other enviroment other than 'dev'  parameterization was introduced and tested in the feature branch **IMAGE 25 
![25](https://user-images.githubusercontent.com/91284177/156927330-658a4cb3-f8a2-439b-b4d5-b0daa685f673.png)

**CI/CD PIPELINE FOR TODO APPLICATION
Prepared Jenkins
Forged a todo PHP repo into my GITHUB account. https://github.com/darey-devops/php-todo.git
Installed PHP and installer dependencies **IMAGE 26 & 27
![26](https://user-images.githubusercontent.com/91284177/156928768-ddd4927b-9a67-47e9-9a8b-1c98bfc0aa7f.png)
![27](https://user-images.githubusercontent.com/91284177/156928769-52fc5f57-9567-4398-b08d-3ee03e3052c7.png)

Installed Jenkins plugins and Plot plugin Artifactory plugin

I configured my jfrog/artifactory in the jenkins user interface UI. **IMAGES 28 & 29

![28](https://user-images.githubusercontent.com/91284177/156971831-6f2fc79e-85c0-42f9-8b12-e4ea6a3e7e36.png)
![29](https://user-images.githubusercontent.com/91284177/156971855-b14c5702-9306-49fa-b829-e9c99ae47d11.png)

**Phase 2 – Integrate Artifactory repository with Jenkins

On the database server, I created database and user
Created database homestead;
CREATED USER 'homestead'@'%' IDENTIFIED BY 'sePret^i';
GRANT ALL PRIVILEGES ON * . * TO 'homestead'@'%';

**IMAGE 30
![30](https://user-images.githubusercontent.com/91284177/157085055-9184b8e8-6222-43fb-bbbe-1f89cefdce9a.png)

A new php-todo pipeline was added to jenkins via blue ocean **IMAGE31
![31](https://user-images.githubusercontent.com/91284177/157086103-b856a93a-0ef4-4a62-95b3-45341be1e5d9.png)

Updated the Jenkinsfile to include dependencies and Unit tests **IMAGES 32 & 33

![32](https://user-images.githubusercontent.com/91284177/157086323-9beec092-2e13-4d37-9439-f47256e5f294.png)
![33](https://user-images.githubusercontent.com/91284177/157086353-2305c30c-0f1d-4f8a-a3d1-415817e463ae.png)

**Phase 3 – Code Quality Analysis

Code analysis and Plot Code Coverage Report were added to the php-todo pipeline. **IMAGE 34
![34](https://user-images.githubusercontent.com/91284177/157088687-9d3fa39b-dee7-4abe-8fb2-15cff0658414.png)

A Plot menu item with chart was configured. **IMAGE 35 & 36
![35](https://user-images.githubusercontent.com/91284177/157089395-d9b20cc4-ae69-4d6d-852b-3bb5afa18054.png)
![36](https://user-images.githubusercontent.com/91284177/157089491-86ee88de-1cc4-475e-b483-784612d8f288.png)

I bundled the application code into an artifac, oploaded to artifactory. Published the resulted artifact into Artifactory. **IMAGE 37 & 38
![37](https://user-images.githubusercontent.com/91284177/157091881-87097b80-1bdb-4815-a732-bb1a91334b6a.png)
![38](https://user-images.githubusercontent.com/91284177/157743500-b7853a32-455f-43c9-9679-6e17bf170ea3.png)

'deployment to dev enviroment' was added to the php-todo jenkins file and was runned successfully by jenkins. I configured php-todo jenkins file to load the ansible-config-mgt playbook  **IMAGES 39, 40  & 41 . 

![39](https://user-images.githubusercontent.com/91284177/157744924-d7da55da-fee4-44b3-bbf7-796d30d5e785.png)

![40](https://user-images.githubusercontent.com/91284177/157744933-b84438bf-b6ca-47dd-bee0-ddd827d1be54.png)
![41](https://user-images.githubusercontent.com/91284177/157745053-e7d142f4-5d03-4d30-b201-050905566e6c.png)

Sonarqube was successfully runned and added to the php-todo jenkinsfile to break the built pipleline from completing when with Bugs. **IMAGE 42 & 43
![42](https://user-images.githubusercontent.com/91284177/157746202-a1a19f2a-2848-4e68-b300-5085bac5ae41.png)
![43](https://user-images.githubusercontent.com/91284177/157760916-031118c3-2848-491f-80cc-73f55a38ff20.png)

Slave agent was added to jenkins to carry some work load randomly depending on availabilty. **IMAGE 44 
![A](https://user-images.githubusercontent.com/91284177/157761141-2f920380-8bad-4454-b7a2-5ca3cbebaf70.png)

I configured webhook between Jenkins and GitHub to automatically run the pipeline when there is a code to be pushed. **IMAGE 45
![45](https://user-images.githubusercontent.com/91284177/157761233-5c8848af-5854-402f-83a5-132e50ca5f61.png)

