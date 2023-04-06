FROM ubuntu:focal
# 우분투 이미지를 도커 허브에서 가져와라(18.04)
LABEL "com.github.actions.name"="Send Webex Message to Room"
LABEL "com.github.actions.description"="Send a message to the given room on Webex"
LABEL "com.github.actions.icon"="message-circle"
LABEL "com.github.actions.color"="orange"

LABEL "repository"="http://github.com/justinyoo/send-webex-message-to-room"
LABEL "homepage"="http://github.com/justinyoo"
LABEL "maintainer"="Justin Yoo <no-reply@aliencube.com>"
# LABEL은 메타데이터 영역
# Install curl
RUN apt-get update && apt-get install -y \
    sudo \
    curl \
 && rm -rf /var/lib/apt/lists/*
# 캐시 삭제하라
ADD entrypoint.sh /entrypoint.sh
# 도커 컨테이너에 추가하라
RUN chmod +x /entrypoint.sh
# 실행권한 줘라
ENTRYPOINT ["/entrypoint.sh"]
# 이걸 실행하라