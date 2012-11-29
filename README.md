# Sample GRAD Math Test

A quiz interface for the MN GRAD math test.  Sample test from: http://www.mnstateassessments.org/itemsamplers.html

## Data

* Data manually parsed from the [24pt Math Test](http://www.mnstateassessments.org/resources/ItemSamplers/GRAD_MATH_SAMPLER_24PT.pdf).
* Answers determined manually from MinnPost.

## Data processing

First convert to JSON

  csvjson application/data/questions.csv > application/data/questions.json```

Then to JSONP for hosting remotely

   echo "grad_callback(" > application/data/questions.jsonp && \
   cat application/data/questions.json >> application/data/questions.jsonp && \
   echo ");" >> application/data/questions.jsonp;