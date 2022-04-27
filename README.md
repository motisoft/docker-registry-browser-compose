# Introduction 
This tool lets you pull and push images on a centralized private registry (your private network docker hub).
this is a very specific setup with ssl, registry browser, and a NAS CIFS/SMB share storage for backup purposes.

## Getting Started
1.	Install docker and docker compose
2.	change the parameters in .env file and replace the certificates in certs directory with your own (there are dummy files there right now)
3.	cd to the registry directory
4.	run `docker compose up -d`

## Usage
1. run `docker tag hello-world your-domain/hello-world`
2. run `docker push your-domain/hello-world`
3. run `docker pull your-domain/hello-world`
4. Done.

## Resources
* [Docker Registry Browser](https://github.com/klausmeyer/docker-registry-browser) lets you browse the contents of your registry.
* [AWS Gallery](https://gallery.ecr.aws/) is alternative public registry for docker images, because docker hub have a rate limit unless you run the command docker login and not exceeding your plan.
