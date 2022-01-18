# BCBR
<img src="https://github.com/fdrepo/www.flutterdoctor.com/blob/99ed3004fceb2fa646efc2cb1d07ef30936d92c2/icons/BCBRCBlue.png" width="100">

## Basic Course in Biomedical Research 
* Its is a Mandatory course conducted by IIT madras, for MD/MS students and faculty.
* It is conducted in Cycles. Questions, answers and chapters are improved every cycle.  
* It covers topics which are essential process and concepts of medical research.
* BCBCR Ongoing Cycle  : [BCBCR 5th Cycle](https://onlinecourses.nptel.ac.in/noc21_md05/preview)

# Apps
[BCBR Q Bank](https://github.com/fdrepo/flutterdoctor.com/blob/0ae8871898c3ac858bf4b86bc87185797398ae48/docs/BCBR/BCBR_Q_Bank.md)

# Design

```mermaid
sequenceDiagram
    participant ODB as Online DB
    participant A as OTP Auth
    participant LDB as Local DB
    participant U as User
    participant Set as Settings
    participant B as Bookmarks
    participant P as Pinned to Board
    participant MCQ as Choice Question
    A->>U: Get UID
    U->>LDB: Set UID in LDB
    U->>ODB: Set UID in OBD 
    ODB->>U: Old Settings / never set (null) 
    U->>LDB: Set Old Setting / never set (null)
    LDB->>Set: Theme Selected
    LDB->>B: BookMarked MCQ
    LDB->>P: Pinned Settings
```

[<< go back to F.d. home](README.md)
