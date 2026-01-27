FROM jenkins/jenkins:lts

COPY --chown=jenkins:jenkins ./plugins.txt /usr/share/jenkins/ref/plugins.txt.override
RUN ln -s /usr/share/jenkins/ref/plugins.txt.override /usr/share/jenkins/ref/plugins.txt && jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

COPY --chown=jenkins:jenkins ./jenkins-iac/jenkins.yaml /usr/share/jenkins/ref/jenkins.yaml.override