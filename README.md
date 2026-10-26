# DUEPL

This article provides executables of all frameworks and all datasets used in our research of Damped Uncertain Erasable Pattern Analysis.

The executables include all the frameworks, such as DUEPL, LUEID, MED*, DEPL, and DWEL* and all the datasets which are used in our experiment: QPMP, Cosmetics, AGM, RTVCQ, AEP, AQ, and T10I4D200K—T10I4D1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the name of the executable for each algorithm is as follows:

| Original Name   | DUEPL | LUEID | MED* | DEPL | DWEL* | 
| --------------- | ----- | ----- | ---- | ---- | ----- | 
| Executable Name | DUEPL | LUEID | MED  | DEPL | DWEL  | 

2. The parameters of the executables are as follows:

 for DUEPL and MED*
```bash
[0]          [1]            [2]                         [3]                           [4]               [5]               
[Executable] [Threshold(%)] [Uncertain Data Path(.txt)] [Transaction Data Path(.dat)] [Division Number] [Decaying Factor]
```

for LUEID
```bash
[0]          [1]            [2]                         [3]                           [4]              
[Executable] [Threshold(%)] [Uncertain Data Path(.txt)] [Transaction Data Path(.dat)] [Division Number]
```

for DEPL
```bash
[0]          [1]            [2]                           [3]               [4]                             
[Executable] [Threshold(%)] [Transaction Data Path(.dat)] [Division Number] [Decaying Factor] 
```

for DWEL*
```bash
[0]          [1]            [2]                           [3]                      [4]               [5]               
[Executable] [Threshold(%)] [Transaction Data Path(.dat)] [Weight Data Path(.txt)] [Division Number] [Decaying Factor] 
```

3. Next, the characteristics of each dataset are as follows:

|  Dataset     | Number of Products| Number of Items | Average Product Size       |
| ------------ | ----------------- | --------------- | -------------------------- |
| QPMP         | 737,453           | 206             | 23.0                       |
| Cosmetics    | 114,635           | 68,604          | 12.8                       |
| AGM          | 9,235             | 62              | 7.0                        |
| RTVCQ        | 6,378             | 76              | 7.6                        |
| AEP          | 10,162            | 130             | 26.0                       |
| AQ           | 9,204             | 130             | 11.2                       |
| T10I4D200K   | 200,000           | 1,000           | 10.0                       |
| T10I4D400K   | 400,000           | 1,000           | 10.0                       |
| T10I4D600K   | 600,000           | 1,000           | 10.0                       |
| T10I4D800K   | 800,000           | 1,000           | 10.0                       |
| T10I4D1000K  | 1,000,000         | 1,000           | 10.0                       |

The datasets can be found at https://drive.google.com/file/d/1rdFdii2a6Cx5DCBdtOWs4hncaQe7k1qf/view?usp=sharing.

4. For example
```bash
DUEPL.exe 2 ..\Data\AGM(unc).txt ..\Data\AGM.dat 10 0.99998 
```
will run DUEPL on AGM, with the threshold set to 2%, the division number set to 10, and the decaying factor set to 0.99998.
```bash
LUEID.exe 0.25 ..\Data\QPMP(unc).txt ..\Data\QPMP.dat 10 
```
will run LUEID on QPMP, with the threshold set to 0.25% and the division number set to 10.
```bash
DEPL.exe 1 ..\Data\RTVCQ.dat 10 0.99998 
```
will run DEPL on RTVCQ, with the threshold set to 1%, the division number set to 10, and the decaying factor set to 0.99998.
```bash
DWEL.exe 1 ..\Data\AQ.dat ..\Data\AQ(wei).txt 10 0.99999 
```
will run DWEL on AQ, with the threshold set to 1%, the division number set to 10, and the decaying factor set to 0.99999.
