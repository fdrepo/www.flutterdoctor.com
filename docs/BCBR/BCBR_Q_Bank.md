# BCBR
<img src="https://github.com/fdrepo/www.flutterdoctor.com/blob/99ed3004fceb2fa646efc2cb1d07ef30936d92c2/icons/BCBRCBlue.png" width="100">

## Basic Course in Biomedical Research 
* Its is a Mandatory course conducted by IIT madras, for MD/MS students and faculty.
* It is conducted in Cycles. Questions, answers and chapters are improved every cycle.  
* It covers topics which are essential process and concepts of medical research.
* BCBCR Ongoing Cycle  : [BCBCR 5th Cycle](https://onlinecourses.nptel.ac.in/noc21_md05/preview)

# Apps
[BCBR Q Bank](https://github.com/fdrepo/flutterdoctor.com/blob/0ae8871898c3ac858bf4b86bc87185797398ae48/docs/BCBR/BCBR_Q_Bank.md)

# CloudDB Design

```mermaid
sequenceDiagram
    participant OLCDB as Common table
        Note left of OLCDB: IMMUTABLE (S3 Bucket Link)
        Note left of OLCDB: uniqueMCQ<UMCQID:Question<String>>
        Note left of OLCDB: uniqueMCQOptions<UMCQID:Options<String:Bool>>
        Note left of OLCDB: uniqueTagsSet<UMCQID:Set<Tag>>
        Note left of OLCDB: uniqueFactoidTweet<UMCQID:List<UFaT>>
        Note left of OLCDB: uniqueTags<Set<Tag>>
        Note right of OLCDB: MUTATING
        Note right of OLCDB: checkUserTags<UUMCQID:List<Tags>>
        Note right of OLCDB: uniqueFactoidTweet<UUMCQID:List<UFaT>>
    participant OLUDB as USER table
        Note right of OLUDB: USER DATA MUTATING
        Note right of OLUDB: uniqueUserID<mobileNumber>
        Note right of OLUDB: uniqueUserName<UUID,UserName>
        Note right of OLUDB: uniqueUserUUMCQID<CONCAT(UUID+MCQID)>
        Note right of OLUDB: uniqueBookMarks<UUMCQID<List<UUMCQID>>>
        Note right of OLUDB: uniquePinnedSettingsUUID<<List<namedSetting>>>
```

# M-MV Design



[<< go back to F.d. home](README.md)
