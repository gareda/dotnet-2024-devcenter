FROM mcr.microsoft.com/deployment-environments/runners/core:latest

RUN wget -O terraform.zip https://releases.hashicorp.com/terraform/1.8.5/terraform_1.8.5_linux_amd64.zip
RUN unzip terraform.zip && rm terraform.zip
RUN mv terraform /usr/bin/terraform

COPY scripts/* /scripts/
RUN find /scripts/ -type f -iname "*.sh" -exec dos2unix '{}' '+'
RUN find /scripts/ -type f -iname "*.sh" -exec chmod +x {} \;
