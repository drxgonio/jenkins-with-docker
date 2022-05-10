# jenkins-with-docker

## Installation
Tutorial set up jenkins for MacOS

After set up docker for mac success
you can pull images jenkins: 

```sh
docker pull jenkins/jenkins
```
You can see images on docker desktop.
or you can type on terminal with:
```sh
docker images
```
After you pulled Jenkins successful. You need write to folder in local with:

```sh
docker run -d -p 49001:8080 -v $PWD/jenkins:/var/jenkins_home -t jenkins/jenkins
```
Output: 5b9b4bee0f0dd08f773183f2460a902597d2d8233c6224bc9dafcc9c584496dd

And excuted code:

```sh
docker run -p 49001:8080 -t jenkins/jenkins
```
Go to browser, access link: http://localhost:49001/

This is where we begin Jenkins installation.

This screen means that a password has been generated in the container’s /var/jenkins_home/secrets/initialAdminPassword file. You need to get that password to enter here. Since, I have mapped the /var/jenkins_home directory in the container with the /User/TriPhan/jenkins directory, I just need to open the /User/TriPhan/jenkins/secrets directory so I can get the password in the initialAdminPassword file to fill.

Open finder -> Select Go -> Select Home... In this here.. you can see folder Jenkins and get password in here.
Jenkins/secrets and open file initialAdminPassword.
