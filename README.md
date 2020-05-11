# git-jenkins
Link to the article: https://tinyurl.com/y89ulw5n
I have created end-to-end auto deployment system using
1. Git & GitHub - as SCM (Source Code Management)
2. Docker - as web hosting for testing & production environment
3. Jenkins - to create job for automation and integration.
I have even created build and delivery pipeline to visualize the flow of process.
In this use case the auto deployment starts as soon as the developer commit from local repository, the automation push to GitHub then deploy it in testing environment, automatic test for it's working, if positive then merge the developer branch to master and the host the production environment through master.😉✌
We will see an use case where we want end-to-end automation which starts from the developer. Once the developer commit his code from Git it will be automatically pushed to GitHub repository, from there, jenkins will copy the files uploaded automatically and host the web page through docker container as testing environment. Once web page is hosted through docker, jenkins will test the web page by very basic http error request (we can modify it further more), once its "200 ok" it will launch an production environment and host it using docker and using ngrok (to create tunnel to save cost on buying domain name and ip address) we will make it available to our clients.

So we have the following job to perform:

1. production- here we will host finally after testing.
2. testing- here we will host the web site in testing environment.
3. qatpass- Quality Assurance Team gives PASS certificate to launch it in production environment after testing. Here we will merge the    developer repository to master repository because master repository will be hosted to production environment.
4. auto testing- here we will test for "200 ok".
