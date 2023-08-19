FROM registry.access.redhat.com/ubi9/ubi:9.2

RUN yum install -y --nodocs dotnet-sdk-6.0 dotnet-sdk-7.0 git zsh

RUN groupadd vscode && useradd -m -g vscode vscode && usermod -aG wheel vscode
RUN echo vscode:vscode | chpasswd
RUN sed -i 's/^#auth/auth/g' /etc/pam.d/su
