FROM jenkins/jenkins:lts-alpine

ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
 
COPY security.groovy /usr/share/jenkins/ref/init.groovy.d/security.groovy
COPY jenkins-user /run/secrets/jenkins-user
COPY jenkins-pass /run/secrets/jenkins-pass

RUN jenkins-plugin-cli --plugins workflow-job workflow-aggregator credentials-binding configuration-as-code git pipeline-model-definition github-branch-source:1.8




