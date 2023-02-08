# VideoReorder Dataset
## Introduce
This dataset is based on Hierachal-MovieNet for video reorder task.
We use 228 movie to generate 10031 movie clips. 7048 clips for train, 589 for val, 1178 for in_domain test and 1196 for out_domain test.

## Download
You can download the full dataset(9.5G) here: https://bigai-research.s3.us-west-1.amazonaws.com/VideoReorder-MovieNet.zip

## Structure
```
.
├── train/
│   ├── 0/
│   │   ├── 0_0.png
│   │   ├── 0_1.png
│   │   ├── ...
│   │   ├── subtitle.json
│   │   ├── info_suffled.json
│   │   └── info.json
│   ├── 1/
│   │   ├── 1_0.png
│   │   ├── 1_1.png
│   │   ├── ...
│   │   ├── subtitle.json
│   │   ├── info_suffled.json
│   │   └── info.json
│   └── ...
│
├── movie_id
├── clip_id.json
├── movie_info.json
├── test/
├── val/
├── tools/
└── README.md
```

## Format
### info.json
```
{
    "tt_id" : "tt0047396",
    "img_id" : 0,
    "shot_id" : [4, ...]
    "scene_id" : [2 , ...]
}
```
### subtitle.json
```
[
    ["Men, are you over 40?"],
    ["When you wake up in the morning, do you feel tired and rundown?"],
    ...
]
```

## Requirements
1. The frames have subtitle in a clip is more than 80\%.
2. The length of a clips is 10 to 20.
3. Only the subtitle that locate on the frame will be record.
4. Out_domain test groups come from different movies with in_domain groups(train,val,test_in_domain), while in_domain groups sampled from same movies  source.
5. NO overlap

   
## statistic
| shot/scene length  | all | train | val | test_in_domain | test_out_domain | 
| --- | :---: | :---: | :---: | :---: | :---: | 
|  1 |    0/6833| 0/4785 | 0/381 | 0/824  | 0/843 |
|  2 |    0/1975| 0/1418 | 0/136 | 0/216  | 0/205 |
|  3 |    0/ 722| 0/518  | 0/44 | 0/84  | 0/76 |
|  4 |  390/ 282| 281/203|19/19 | 52/27  | 38/33 |
|  5 | 1304/ 113| 946/79 | 75/8 | 137/10  | 146/16 |
|  6 | 1732/  52| 1180/31|112/1 | 219/7  | 221/13 |
|  7 | 1647/  24| 1164/14|90/0 | 182/6  | 211/4 |
|  8 | 1228/  10| 900/9  | 82/0 | 134/1  | 172/0 |
|  9 |  937/   8| 653/4  |59/0 | 113/2  | 112/2 |
| 10 |  767/   5| 562/2  | 38/0 | 85/1  | 82/2 |
| 11 |  626/   2| 447/2  | 37/0 | 68/0  | 74/0 |
| 12 |  457/   1| 335/0  | 28/0 | 56/0  | 38/1 |
| 13 |  326/   1| 224/1  | 21/0 | 48/0  | 33/0 |
| 14 |  245/   2| 170/1  | 17/0 | 30/0  | 28/1 |
| 15 |  169/   1| 114/1  | 9/0 | 26/0  | 20/0 |
| 16 |   74/   0| 48/00  | 1/0 | 13/0  | 12/0 |
| 17 |   48/   0| 29/0   | 0/0 | 11/0  | 8/0 |
| 18 |   17/   0| 11/0   | 1/0 | 4/0  | 1/0 |
| 19 |    4/   0| 4/0    | 0/0 | 0/0  | 0/0 |
