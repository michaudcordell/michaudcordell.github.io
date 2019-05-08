---
layout: page
title: Benthic Species Detector
permalink: /projects/benthicspeciesdetector
---

![Benthic Species Detector Logo](../images/benthic_species_detector_logo.png)

BenthicSpeciesDetector is a class that detects squares, rectangles, triangles, and 
circles/ellipses from an image, for the purpose of completing the benthic species 
detection task in the 2019 MATE underwater robotics competition. It accomplishes this 
task through the following sequence of steps:
* Generate object proposals using Selective Search, and filter the proposals to the 
  minimum amount of bounding rectangles that probably contain shapes
* Detect corners within the image, and assign each to the bounding rectangle to which 
  it belongs
* Further filter bounding rectangles which contain too many corners to be a benthic 
  species shape
* Assign a score for each considered benthic species shape to the shape within each 
  bounding rectangle using a combination of corner count, pixel area, and central and 
  interior angles
* Filter shape scores that are below a particular threshold
* Take the highest score for each bounding rectangle as the most probable benthic species

Github link: [Benthic Species Detector](https://github.com/michaudcordell/BenthicSpeciesDetector)
