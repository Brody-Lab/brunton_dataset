# Data Set from Brunton, Botvinick, and Brody Science 2013

This repository contains the rat behavioral data set used in [Brunton, Bingni W., Matthew M. Botvinick, and Carlos D. Brody. 2013. “Rats and Humans Can Optimally Accumulate Evidence for Decision-Making.” Science 340 (6128): 95–98.](http://dx.doi.org/10.1126/science.1233912)

Each file corresponds to data from 1 rat (19 rats total). Each file is named "chrono\_{ratname}\_rawdata.mat" and is a [Matlab](https://www.mathworks.com/products/matlab.html) data file. (Note that such files can also be read into Python or Julia.)

Loading a file into a variable will instantiate a structure with the following fields:

* ratname -- Identifies an animal subjecy
* daterange -- The date range over which the data was gathered
* rawdata -- The actual data
* total_trials -- Number of behavioral trials in the data set
* avgdata -- Data averaged within trial conditions.

Most of the data is in the "rawdata" field, which in turn is a structure with a number of fields, each of which contains a total_trials-long vector. The i'th entry corresponds to the i'th trial. The fields are the following:

* stim_delay -- silent period, in seconds, between subject poking its nose into the center poke, and the stimulus starting to play
* T -- duration, in seconds, over which auditory clicks were played
* leftbups -- times, relative to the start of the stimulus period, at which clicks from the left speaker were played
* rightbups -- times, relative to the start of the stimulus period, at which clicks from the right speaker were played
* pokedR -- Boolean indicating whether the subject, as its response, decided to poke into the Right poke at the end of the stimulus (true), or poked into the left poke (false)
* hit -- Boolean indicating whether the subject's response poke was correct (rewarded) or incorrect (not rewarded)
* Delta -- totel number of Right minus Left clicks played
* gamma -- logarithm of the ratio of the Poisson rate used to generate Right versus Left clicks

