nao-datasets
============

This repository contains data collected by the Aldebaran Robotics NAO
robot with the hope that it will help people develop NAO applications
that process sensor data. Each sub-directory contains one dataset with
its own README describing the data.

The first two datasets were captured using the NAO wanderer software (https://github.com/davesnowdon/nao-wanderer/)

I've also included the python HTTP server that I used to collect the
data (running on my laptop) and an example python client that shows how
to send an HTTP POST request - see src/main/python/data_collector). All
the code uses only standard python libraries.

Each data set contains the following:
* A README file explaining what the data is
* For each snapshot (approximately once per second) a JPG image taken
  from NAO's camera and a JSON file containing sensor data. Each file
  has a common prefix and an index value that indicates its place in the
  sequence.
* Each JSON file contains a timestamp, left & right sonar values and the
  position of the robot in world coordinates (as reported by NAOqi).
* A video file (or link to one) showing NAO moving about the space -
  this is not intended for automated analysis but as an aid to
  understanding the data. It is recommended that new datasets don't
  include the actual video file but instead have a README that contains
  a link to the file hosted on a service such as youtube or vimeo.

If you have data sets that you would like to contribute please do one of the following:
* Fork the project on github and send me a pull request
* Create an issue for the project indicating what the data set is and
  where I can obtain it.

Please only send data that you have personally collected and own the
copyright for. Please include a description of what is in the data
set. For machine readable data please use JSON format and standard
formats for any audio, image or video data.

I'd also welcome:
* Suggestions of what data to collect (including sensor values that people would like to see collected and ideally code that collects those values)
* Code for data collection & analysis.
* Suggestions of how to improve my data collection technique
