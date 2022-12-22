# Twitter Event Data (TED)
These data sets consist of tweet IDs of collected data and keywords which describe the events occurred during the selected time frames as ground truth. More details about the data sets can be found from the reference paper <strong>"[Embed2Detect: Temporally Clustered Embedded Words for Event Detection in Social Media](https://link.springer.com/article/10.1007/s10994-021-05988-7)"</strong> <br>
If you use these data sets in your research, please consider citing this paper and reference details are given below.

### Available data sets
- MUNLIV - English Premier League 19/20 on 20 October 2019 between Manchester United and Liverpool
- BrexitVote - Brexit Super Saturday 2019 on 19 October 2019

### Folders and files
- ground_truth - folder which contains ground truth labels as a set of .txt files named using starting time of event 
occurred time window
- time_windows - folder which contains the data correspond to the time windows
- ids_<start_time>-<end_time>.txt - file which contains the IDs of all extracted tweets during the mentioned time 
(start_time-end_time)

### Ground truth format
- Time periods of ground truth events are mentioned as the name of .txt file <br>
For MUNLIV, 2 minute time windows and for BrexitVote, 30 minute time windows are considered. 
(e.g. in MINLIV, 2019_10_20_15_30 represents the time window 2019-10-20 15:30 - 15:32 )
- Keywords related to an event are mentioned in a single line in .txt file
- Synonym (similar) words are grouped using [] (e.g. <b>[</b>kick off,kickoff,kick-off<b>]</b>) <br>
Identification of at least one word from a synonym word group will be sufficient during event keyword match
- Duplicate event keyword sets are separated using | (e.g. [full time,full-time,fulltime,FT][1-1,draw]<b>|</b>[over,end][1-1,draw]) <br>
Identification of keywords in one duplicate set will be sufficient during event identification

### Notes
- All times mentioned with data sets and ground truth are in Coordinated Universal Time (UTC)

### Reference
```
@article{hettiarachchi2021embed2detect,
  title={{E}mbed2{D}etect: temporally clustered embedded words for event detection in social media},
  author={Hettiarachchi, Hansi and Adedoyin-Olowe, Mariam and Bhogal, Jagdev and Gaber, Mohamed Medhat},
  journal={Machine Learning},
  volume={111},
  pages={49--87},
  year={2022},
  publisher={Springer},
  doi = {10.1007/s10994-021-05988-7},
  url = "https://doi.org/10.1007/s10994-021-05988-7",
}
```

### Extensions
TED with sentiment labels is available as [TED-S](https://github.com/HHansi/TED-S).
