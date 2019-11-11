This is a proof of concept Java implementation of our Framework for Immune Applications through Application-level Unsupervised Outlier-based Intrusion Detection and Prevention.

**Dependencies**

All dependencies are managed through Docker and Gradle. Docker is all what you need, while Gradle distribution will be automatically fetched by Gradle wrapper, which will be downloaded from this repository by Docker.

**Structure**
- docker: hosts Dockerfile, all what you need to build your development and test environment
- evaluation: outlier detection evaluation, currently based on R-precision
- framework: our framework implementation
- models: folder to host models generated by our framework for each immunized/instrumented application

**How To**
- Make sure you have Docker installed
- docker build -t immune-apps:1.0 https://raw.githubusercontent.com/oiraqi/immune-apps/master/docker/Dockerfile
- docker run --name immune-apps-container -p 8443:8443 -it immune-apps:1.0
- cd immune-apps/scripts
- ./ofbiz-immunizer-agent.jar
