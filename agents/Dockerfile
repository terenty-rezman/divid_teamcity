ARG TEAMCITY_VERSION
FROM jetbrains/teamcity-agent:${TEAMCITY_VERSION}-linux-sudo

ENV REMEMBER_USER=${USER}

USER root
RUN apt-get update && apt-get install -y \
    python3-pip

USER ${REMEMBER_USER}
