FROM library/ubuntu:20.04
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get -y install python3-pip curl unzip openjdk-11-jdk
RUN curl -fsSL https://raw.githubusercontent.com/databricks/setup-cli/main/install.sh | sh
RUN pip install requests 
COPY my_mlops_project/requirements.txt .
COPY test-requirements.txt .
RUN pip install -r requirements.txt
RUN pip install -r test-requirements.txt
