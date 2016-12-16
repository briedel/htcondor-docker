[![Docker Automated buil](https://img.shields.io/docker/automated/lincolnbryant/coreos-osg-wn.svg)]()


#htcondor-docker

this is our kustomized worker node image that connects to a fixed htcondor
central manager. the intent here is to run HTCondor as a container while
using it to launch more containers.

##usage
edit the condor config to your liking, and then
```
docker build . 
docker run --net=host -v /var/run/docker.sock:/var/run/docker.sock \ 
-v /var/lib/condor:/var/lib/condor -v /cvmfs:/cvmfs:slave <image id> 
```

##thanks

thanks to Andy Pohl @ UW-Madison for building the first version of this
dockerfile that I have thoroughly butchered.
