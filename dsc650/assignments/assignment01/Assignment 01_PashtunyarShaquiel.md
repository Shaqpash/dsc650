---
title: Assignment 1
subtitle: Computer performance, reliability, and scalability calculation
author: Shaquiel Pashtunyar
03/19/2023
---

## 1.2 

#### a. Data Sizes

| Data Item                                  | Size per Item | 
|--------------------------------------------|--------------:|
| 128 character message.                     | 128 Byte       
| 1024x768 PNG image                         | 4.72 MB       |https://toolstud.io/photo/filesize.php?imagewidth=1024&imageheight=768
| 1024x768 RAW image                         | 1.18 MB       | 
| HD (1080p) HEVC Video (15 minutes)         | 2500MB      |https://toolstud.io/video/filesize.php?width=1920&height=1080&framerate=24&timeduration=15&timeduration_unit=minutes&compression=19290&specificbitrate=100&specificbitrate_unit=1000000
| HD (1080p) Uncompressed Video (15 minutes) | 15600 MB       |
| 4K UHD HEVC Video (15 minutes)             | 2550 MB       |170MB per 60 seconds (1 minute) so 170MB*15minutes = 2550 MB
| 4k UHD Uncompressed Video (15 minutes)     | 3660 MB       |
| Human Genome (Uncompressed)                |  6.27 GB      |https://www.google.com/search?q=uncomprtessed+human+genome+size&rlz=1C1CHBF_enUS997US997&oq=uncomprtessed+human+genome+size&aqs=chrome..69i57j33i10i160j33i299.4955j0j4&sourceid=chrome&ie=UTF-8

#### b. Scaling

|                                           | Size     | # HD | 
|-------------------------------------------|---------:|-----:|
| Daily Twitter Tweets (Uncompressed)       | 64GB     | 1    | 128*500 64,00bytes=0.064 MB *1,000,000= 64000mb mb to gb= 64Gb*3 copies =192GB
| Daily Twitter Tweets (Snappy Compressed)  | 37.5     | 1    |  64/1.7
| Daily Instagram Photos                    | 354TB    |   36 |  4.72*75000000
| Daily YouTube Videos                      | 500TB    |  50  | 500  * 60  = 30000 mins. 15 min = 2500MB, 30000/15 = 2000, 2000 * 2500 = 5000000MB = 500 TB
| Yearly Twitter Tweets (Uncompressed)      | 23.36TB  |   3  | 64 GB * 365 = 23360 GB = 23.36 TB, 23.36 or 3 Harddrives
| Yearly Twitter Tweets (Snappy Compressed) | 13.7     |   2  | 37.65 GB * 365 = 13742.25 GB = 13.75 TB, 13.75  or round up = 2 HD
| Yearly Instagram Photos                   | 41062.5TB|  4107 |112.5 TB (daily) * 365 = 41062.5 TB, 41062.5 or round up = 4107 HD
| Yearly YouTube Videos                     | 182500TB |  18250 | 500 TB * 365 = 182500 TB, 182500 or 18250 HD

#### c. Reliability
|                                    | # HD | # Failures |
|------------------------------------|-----:|-----------:|
| Twitter Tweets (Uncompressed)      | 3    |   0.0255   |
| Twitter Tweets (Snappy Compressed) | 2    |   0.017    |
| Instagram Photos                   | 4107 |   ~35      |
| YouTube Videos                     | 18250|   ~3155    |


Failure rate = 0.85% (https://www.backblaze.com/b2/hard-drive-test-data.html) 
0.0085 * 3 = 0.0255 
0.0085 * 2 = 0.017 
0.0085 * 4107 = 34.9095 
0.0085 * 18250 = 155.125

#### d. Latency

|                           | One Way Latency      |
|---------------------------|---------------------:|
| Los Angeles to Amsterdam  | 140 ms               |
| Low Earth Orbit Satellite | 600 ms               |
| Geostationary Satellite   | 240 ms               |
| Earth to the Moon         | 2560 ms              |
| Earth to Mars             | 13 minutes           | 


https://wondernetwork.com/pings
https://www.omniaccess.com/leo/#:~:text=The%20GEO%20latency%20is%20of,and%20an%20essential%20part%20if
https://www.satsig.net/latency.htm
https://en.wikipedia.org/wiki/Earth%E2%80%93Moon%E2%80%93Earth_communication#:~:text=Propagation%20time%20to%20the%20Moon,milliseconds%20of%20wave%20travel%20time.
https://blogs.esa.int/mex/2012/08/05/time-delay-between-mars-and-earth