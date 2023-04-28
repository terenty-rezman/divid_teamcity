ARG TEAMCITY_VERSION
FROM jetbrains/teamcity-agent:${TEAMCITY_VERSION}-linux-sudo

ENV REMEMBER_USER=${USER}

# install pip for divid_deploy
USER root
RUN apt-get update && apt-get install -y \
    python3-pip

SHELL ["/bin/bash", "-c"]

# need this to disable host confirmation when ssh to unknown host
# https://www.jetbrains.com/help/teamcity/ssh-agent.html
RUN mkdir -p /root/.ssh/ && \
echo $'Host *\n\
\tstrictHostKeyChecking no\n' > /root/.ssh/config

USER ${REMEMBER_USER}
