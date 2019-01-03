# Deep Cloud: A Cloud platform to serve deep/machine learning models for source code modeling tasks.

This repository contains our [CodeGRU](arxive.org) saved model and instructions regarding how a developer can use our "Deep Cloud" platform. "Deep Cloud" help suggest the source code in our Visual Studio Code IDE plugin named "DeepVS" in real time. An online version of Deep Cloud can be found [here](http://104.194.70.175/). You can find our "DeepVS" tool [here]( https://github.com/yaxirhuxxain/DeepVS).

## Deep Cloud Usage
To integrate our Deep Cloud platform with your own IDE plugin interface please follow these instructions. Deep Cloud accepts a simple GET request and returns a JSON object with top 3 predictions based on "CodeGRU" model. You can simply send a GET request at "104.194.70.175/deepvs?code=<your-code>". Here <your-code> refers to the source code context from which you want the next source code suggestion. 

#Example: 
104.194.70.175/deepvs?code="for(Int IntVar" 
Here "for(Int IntVar" refers to the context and Deep Cloud will respond a JSON object "['=', ':', ';']" containing top 3 suggestions.

## Server/Local platform
A developer can implement its own Server/local platform to serve deep learning models for various tasks. A software developer can simply implement a web interface similar to "Deep Cloud" which can accept the source code context and send back the response in JSON format. For better understanding of our Deep Cloud or DeepVS tool we suggest to read our paper [here](arxive.org).

## Technical Details
Our Deep Cloud is a platform as a service [PAAS](https://www.dummies.com/programming/cloud-computing/hybrid-cloud/what-is-platform-as-a-service-paas-in-cloud-computing/) based cloud. Deep Cloud consists of a single core Intel CPU with 512mb Ram and 10GB hard disk running ubuntu-18 x64-bit non GUI edition. This low level configuration of our Deep Cloud makes it possible to run it on any low end platform (local computer or server). An online version of Deep Cloud can be found [here](http://104.194.70.175/).

