### codec

```
0x17    23    speaker out
0x16    22    hp out
0x1a    26    Internal Mic in
0x19    25    Mic in
```

```
0x16 > 0x10    22 > 16
0x17 > 0x11    23 > 17

0x13 > 0x1a    19 > 26
0x14 > 0x19    20 > 25
```



```
Description                  Node     PinDefault             
HP Out at Ext Right         22 0x16   0x04211040   
Speaker at Int N/A          23 0x17   0x90170110   
Other at Ext N/A            24 0x18   0x40f001f0   
Mic at Ext Right            25 0x19   0x04a11030   
Mic at Int Top              26 0x1a   0x95a70120   
```



```          bash
16        [Jack]  HP Out at Ext Right        40 10 21 04


17        [Fixed] Speaker at Int N/A         10 01 17 90

19        [Jack]  Mic at Ext Right           30 10 a1 04
1a        [Fixed] Mic at Int Top             20 01 a7 95

18        [N/A]   Other at Ext N/A           f0 01 f0 40
```

```
0x17    23    speaker out
0x16    22    hp out
0x1a    26    Internal Mic in
0x19    25    Mic in
```

```
f0 01 f0 40 > f0 00 00 40



17        [Fixed] Speaker at Int N/A         10 01 17 90
内置扬声器的                                   c10 d01 e10 f90
 

1a        [Fixed] Mic at Int Top             20 01 a7 95
内置麦克风的                                   c20 d01 ea0 f90



16        [Jack]  HP Out at Ext Right        40 10 21 04
耳机扬声器                                    c40 d10 e21 f01


19        [Jack]  Mic at Ext Right           30 10 a1 04
                                             c80 d10 e81 f01
外置麦克风插口


```

```
Codec: Conexant CX20751/2   Address: 0   DevID: 351359247 (0x14f1510f)
```

```
01671c40 01671d10 01671e21 01671f01
01771c10 01771d01 01771e10 01771f90
01871cf0 01871d00 01871e00 01871f40
01971c80 01971d10 01971e81 01971f01
01a71c20 01a71d01 01a71ea0 01a71f90


01671C40 01671D10 01671E21 01671F04 
01771C10 01771D01 01771E17 01771F90 
01971C30 01971D10 01971E81 01971F04 
01A71C20 01A71D01 01A71EA0 01A71F90 
```

