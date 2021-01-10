# Microservices-Store
Fullstack ecommerce store with all necessary microservices.
Using a Microservices approach to ecommerce application with React, NodeJs, Docker and Kubernetes.

To start each of the services, `cd` into that folder then do `npm install` and `npm start`.


### Project Setup

    $ npm install -g nodemon

    $ cd service

    $ npx create-react-app service

<br/>

    $ cd service

    $ mkdir posts
    $ cd posts
    $ npm init -y

    $ npm install --save express cors axios

<br/>

    $ cd service

    $ mkdir comments
    $ cd comments
    $ npm init -y

    $ npm install --save express cors axios

<br/>
Same is followed for creation of Client,event-bus,posts and query.

### Testing all Service using Postman

<br/>

    $ curl \
    --request POST http://localhost:4000/posts/ \
    --header "Content-Type: application/json" \
    | python -m json.tool

<br/>

    $ curl \
    --request GET http://localhost:4000/posts/ \
    --header "Content-Type: application/json" \
    | python -m json.tool

<br/>

### Docker Kubernetes and Skaffold Installation
Install Docker Desktop for your specific machine or Docker Daemon(for Linux Users).<br>
Currently the application doesnt completely support Podman but looking to do that in near time.

For Kubernetes a Kubernetes single cluster can be enabled from Docker Desktop itself as it comes built in.<br>
I am using Minikibe for this project.

<p>Skaffold can be install by running this command in your terminal.

    $ curl -Lo skaffold https://storage.googleapis.com/skaffold/releases/latest/skaffold-linux-amd64 && \
    $ sudo install skaffold /usr/local/bin/

