# Youtube videos 

## explanatory

1. [Intro to Object Detection ](https://www.youtube.com/watch?v=t-phGBfPEZ4)

    object localization vs detection

    history - potential problems:
    1. Sliding windows - a lot of computation (OverFeat paper), many bounding boxes for same object
    2. Regional based networks - slow and complicated because of 2 step process
    3. You Only Look Once - current approach

2. [Intersection over Union](https://www.youtube.com/watch?v=XXYG5ZWtjj0)

    how do we measure how good bounding box is when compared with example
    - calculate intersection
    - calculate union
    - metric: intersection over union 
      -  IoU = intersection / union
      -  ranges: 0.5 0.7 0.9
    - algorithm
      - values increase in directions
        - X to the left
        - Y to the bottom
      - intersection
        - x1 = max(box1[0],box2[0])
        - y1 = max(box1[1],box2[1])
        - x2 = min(box1[2],box2[2])
        - y2 = min(box1[3],box2[3])  
      - union
        - intersection / (box1 + box2 - intersection)
      - box format: midpoint or corners

3. [Non Max Suppression](https://www.youtube.com/watch?v=YDkjWEN8jNA)

    clean up irrelevant boxes 
    - set threshold and delete all boxes below it
    - ...

4. [Mean Average Precision](https://www.youtube.com/watch?v=FppOzcDvaDI)
   
   most common metric to evaluate object detection models
   - "mAP@0.5:0.05:0.95" what does it mean?
   - false positive and true positive, true negatives and false negatives
   - precision and recall
     - precision - what fraction was correct
     - recall - what fraction was detected
     - battle between recall and precision e.g. autonomous car
   - algorithm
     - calculate recall and precision for every box
     - take are of graph
     - do it for every class
     - take average
     - iterate through different IoU thresholds e.g. 0.5,0.55,0.6...0.95 and average results

## tutorials

# Blog posts

