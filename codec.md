### codec

```bash
[   21.181976] snd_hda_codec_conexant hdaudioC1D0: CX20751/2: BIOS auto-probing.
[   21.182265] snd_hda_codec_conexant hdaudioC1D0: autoconfig for CX20751/2: line_outs=1 (0x17/0x0/0x0/0x0/0x0) type:speaker
[   21.182268] snd_hda_codec_conexant hdaudioC1D0:    speaker_outs=0 (0x0/0x0/0x0/0x0/0x0)
[   21.182270] snd_hda_codec_conexant hdaudioC1D0:    hp_outs=1 (0x16/0x0/0x0/0x0/0x0)
[   21.182271] snd_hda_codec_conexant hdaudioC1D0:    mono: mono_out=0x0
[   21.182273] snd_hda_codec_conexant hdaudioC1D0:    inputs:
[   21.182275] snd_hda_codec_conexant hdaudioC1D0:      Internal Mic=0x1a
[   21.182276] snd_hda_codec_conexant hdaudioC1D0:      Mic=0x19
[   21.183057] snd_hda_codec_conexant hdaudioC1D0: Enable sync_write for stable communication
```



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

Verbs from Linux Codec Dump File: codec1

Codec: Conexant CX20751/2   Address: 0   DevID: 351359247 (0x14f1510f)

   Jack   Color  Description                  Node     PinDefault             Original Verbs
--------------------------------------------------------------------------------------------------------
    1/8   Black  HP Out at Ext Right         22 0x16   0x04211040   01671c40 01671d10 01671e21 01671f04
 Analog Unknown  Speaker at Int N/A          23 0x17   0x90170110   01771c10 01771d01 01771e17 01771f90
Unknown Unknown  Other at Ext N/A            24 0x18   0x40f001f0   01871cf0 01871d01 01871ef0 01871f40
    1/8   Black  Mic at Ext Right            25 0x19   0x04a11030   01971c30 01971d10 01971ea1 01971f04
 Analog Unknown  Mic at Int Top              26 0x1a   0x95a70120   01a71c20 01a71d01 01a71ea7 01a71f95
--------------------------------------------------------------------------------------------------------


   Jack   Color  Description                  Node     PinDefault             Modified Verbs
--------------------------------------------------------------------------------------------------------
    1/8   Black  HP Out at Ext Right         22 0x16   0x04211040   01671c40 01671d10 01671e21 01671f00
 Analog Unknown  Speaker at Int N/A          23 0x17   0x90170110   01771c10 01771d00 01771e17 01771f90
Unknown Unknown  Other at Ext N/A            24 0x18   0x40f001f0   01871cf0 01871d00 01871ef0 01871f40
    1/8   Black  Mic at Ext Right            25 0x19   0x04a11030   01971c30 01971d10 01971ea1 01971f00
 Analog Unknown  Mic at Int Top              26 0x1a   0x95a70120   01a71c20 01a71d00 01a71ea7 01a71f90
--------------------------------------------------------------------------------------------------------

Modified Verbs in One Line: 01671c40 01671d10 01671e21 01671f00 01771c10 01771d00 01771e17 01771f90 01871cf0 01871d00 01871ef0 01871f40 01971c30 01971d10 01971ea1 01971f00 01a71c20 01a71d00 01a71ea7 01a71f90
--------------------------------------------------------------------------------------------------------


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

外置麦克风

16        [Jack]  HP Out at Ext Right        40 10 21 04

耳机外放

17        [Fixed] Speaker at Int N/A         10 01 17 90

mic 内部设备

19        [Jack]  Mic at Ext Right           30 10 a1 04

外部设备 耳机? mic 

1a        [Fixed] Mic at Int Top             20 01 a7 95

内部设备
```

```
Codec: Conexant CX20751/2   Address: 0   DevID: 351359247 (0x14f1510f)
```

