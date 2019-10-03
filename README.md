This is a Hackfest project from [Access 2019](https://accessconference.ca), based on Marii Nyrop's [Annotate](https://github.com/mnyrop/annotate) demo. This version adds an instance of SimpleAnnotationServer (in a Docker container) to store the annotations, replacing the use of the browser's local storage. (In this it departs from the minimal computing commitment of the original.)

Create/store/load static annotations on IIIF manifests via Jekyll

## Getting started

### Requirements
- Ruby >=2.2
- Jekyll >=3.5
- Bundler >=1.12

### Installing
- Install [Docker](https://docs.docker.com/install/) according to the instructions for your platform.
- Clone this repository and navigate into it:<br>
  `$ git clone https://github.com/mnyrop/annotate.git && cd annotate`
- Install dependencies:<br>
  `$ bundle install`
- Initialize the SimpleAnnotationServer submodule:<br>
  `$ git submodule update --init --recursive`
- Build and run the Docker container with the Simple Annotation Server (note: this may take several minutes, and will use a lot of network bandwidth):<br>
  `$ cd SimpleAnnotationServer && ./runDocker.sh`<br>
  The annotation server is now online at [http://localhost:8888/annotation/](http://localhost:8888/annotation/)
- To stop the Docker container:<br>
  `$ docker stop sas`