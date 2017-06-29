FROM cahatest76/ubuntu:smart

#COPY . /usr/src/myapp

# Install dependencies
RUN apt-get install -y \
	default-jdk 

# Install Grails
WORKDIR /usr/lib/jvm
RUN wget https://github.com/grails/grails-core/releases/download/v3.2.10/grails-3.2.10.zip && \
	unzip grails-3.2.10.zip && \
	rm -rf grails-3.2.10.zip && \
	ln -s grails-3.2.10 grails

# Setup Grails path.
ENV GRAILS_HOME /usr/lib/jvm/grails
ENV PATH $GRAILS_HOME/bin:$PATH

# Create App Directory
RUN mkdir /app

# Set Workdir
WORKDIR /app

#CMD /bin/bash 

