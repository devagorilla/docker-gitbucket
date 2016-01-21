docker-gitbucket
================


## Usage

To run the container, do the following:

```
% docker run -d -p 8080:8080 -p 29418:29418 -v /gitbucket-data:/gitbucket devagorilla/docker-gitbucket:latest java -jar /opt/gitbucket.war --h2url=jdbc:h2:tcp://H2-ELB-Public-1985951393.us-west-2.elb.amazonaws.com:1521//opt/h2-data/.gitbucket/data
```

You can see gitbucket running on http://localhost:8080/

You also see gitbucket data write out to "./gitbucket-data".

In order to access the git repository over SSH (port 29418), check settings below.

- GitBucket > Administration > System Settings > SSH access

## Building

To build the image, do the following:

```
% docker build github.com/devagorilla/docker-gitbucket
```

A prebuilt container is available in the docker index.

```
% docker pull devagorilla/docker-gitbucket
```

## GitBucket's license
see https://github.com/takezoe/gitbucket
