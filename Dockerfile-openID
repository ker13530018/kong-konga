FROM kong:1.1-centos

LABEL description="Centos 7 + Kong 1.1.2 + kong-oidc plugin"

RUN yum install -y git unzip && yum clean all

RUN luarocks install kong-oidc
