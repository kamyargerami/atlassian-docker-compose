FROM atlassian/jira-software:latest
USER root

# Add proxy unpacking to container
COPY &quotatlassian-agent.jar&quot /opt/atlassian/jira/

# Set Startup Loading Agent Package
RUN echo 'export CATALINA_OPTS=&quot-javaagent:/opt/atlassian/jira/atlassian-agent.jar ${CATALINA_OPTS}&quot' >> /opt/atlassian/jira/bin/setenv.sh
