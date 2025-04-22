# Performance_of_chip_programmers

## SPI operations time:

Tesitng computer: Intel(R) Core(TM)2 Duo CPU     E8400  @ 3.00GHz 5GB RAM

Testing chip: Winbond 25Q32 (4M)

| Programmer |       Software          |  Platform  |  User Interface  | Reading | Erasing |  Writing | Data checking |
| :---       |       :---              |     :---   |      :---        | :---: | :---: | :---: | :---: |
| Raccoon    | Raccoon Flash Explorer Full | Windows, Linux, Android, TV-OS | GUI, Console |  5.5-8.0s  |  Auto when In-Write  |  20.0-23.0s   |   Auto when In-Write/In-Read   |
| Raccoon    | Raccoon Demo/Free version  | Windows, Linux, Android, TV-OS | GUI, Console |  14.0s  |  Auto when In-Write  |  24.0s   |   14.0s   |
| CH341A     | IMSProg v1.4.3           | Linux   | GUI      | 33.9s  | 12.7s | 328.5s | 33.9s   |
| CH341A     | SNANDer v.1.7.8          | Linux   | Console  | 33.0s  | 8.0s  | 327.0s | 33.0s   |
| CH341A     | flashrom v1.2            | Linux   | Console  | 34.6s  | 83.2s | 132.7s | 34.5s   |
| CH341A     | Ch341 Programmer 1.34    | Windows | GUI      | 36.4s  | 9.0s  | 231.4s | 36.4s   |
| CH341A     | NeoProgrammer 2.2.0.10   | Windows | GUI      | 36.7s  | 9.1s  | 220.8s | 36.7s   |
| CH347T	   | ch347-nor-prog	          | Linux   | Console  | 1.1s	  | 0.1s	| 28.9s	 | 1.1s    |
| CH347T	   | CH347_GUI_SPI_NOR_Flash_	| Linux   | GUI	     | 1.6s	  | 9.9s	| 35.0s	 | 13.1s   |
| CH347T	   | СH347 HighSpeed pr.v1.40	| Windows | GUI	     | 0.7s	  | 10.0s	| 8.1s	 | 0.7s    |
| EZP2019+   | EZP2019+ Ver. 2.0        | Windows | GUI      | 33.0s  | 10.4s | 38.7s  | 33.0s   |

## Programmer Hardware features

| Programmer |       Software             |  1.8V Chip support |  Test Clip Support | Overload Protect | Flipped chip protect |  Pins connect checking |  Logic Levels check |  Bus Error check |
| :---       |       :---                 |             :---:  |             :---:  |          :---:   |              :---:   |   :---:                |              :---:  |           :---:  |
| Raccoon    | Raccoon Flash Explorer     | ✔                 | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |
| Raccoon    | Raccoon Demo/Free version  | easy to add       | ✔ | - | - | - | - | - |
| CH341A     | IMSProg v1.4.3             | Need Adapter      | - | - | - | - | - | - |
| CH341A     | SNANDer v.1.7.8            | Need Adapter      | - | - | - | - | - | - |
| CH341A     | flashrom v1.2              | Need Adapter      | - | - | - | - | - | - |
| CH341A     | Ch341 Programmer 1.34      | Need Adapter      | - | - | - | - | - | - |
| CH341A     | NeoProgrammer 2.2.0.10     | Need Adapter      | - | - | - | - | - | - |
| CH347T	   | ch347-nor-prog	            | +/- Need Adapter  | - | - | - | - | - | - |
| CH347T	   | CH347_GUI_SPI_NOR_Flash_	  | +/- Need Adapter  | - | - | - | - | - | - |
| CH347T	   | СH347 HighSpeed pr.v1.40	  | +/- Need Adapter  | - | - | - | - | - | - |
| EZP2019+   | EZP2019+ Ver. 2.0          | Need Adapter      | - | - | - | - | - | - |

## Programmmer software features

| Programmer | Software                |  Platform  |  User Interface  |  SPI NOR| I2C | MW | Edit SR | SFDP view | Security area view |.bin|.hex|.cap|
| :---       |       :---              |     :---   |      :---        |:---:|:---:|:---:| :---:  |   :---:   |   :---:   |:---:|:---:|:---:|
| Raccoon    | [Raccoon Flash Explorer ](https://t.me/racc00n_news)       | Windows, Linux, Android, TV-OS | GUI, Console | ✔   | ✔   | -   |  -     |     -     |  -  | ✔ | - | - |
| Raccoon    | [Raccoon Demo/Free version](https://github.com/lapot2/Raccoon-Flash-Explorer-Demo)       | Windows, Linux, Android, TV-OS | GUI, Console | ✔   | ✔   | -   |  -     |     -     |  -  | - | - | - |
| CH341A     | [IMSProg v1.3.1](https://github.com/bigbigmdm/IMSProg)         | Linux | GUI  | ✔   | ✔   | ✔   |  ✔     |     ✔    |  -  | ✔ | ✔ | ✔ |
| CH341A     | [SNANDer v.1.7.8](https://github.com/McMCCRU/SNANDer)         | Linux | Console  | ✔   |+/-  |+/-  |  -     |     -     |  -  | ✔ | - | - |
| CH341A     | [flashrom v1.2](https://flashrom.org/)           | Linux | Console  | ✔   | -   | -   |  -     |     -     |  -  | ✔ | - | - |
| CH341A     | [Ch341 Programmer 1.34](https://github.com/YTEC-info/CH341A-Softwares/blob/main/Programas/Windows/CH341Programmer/CH341Programmer%20V1.38/Ch341Programmer.exe?ysclid=ls2wxkusch126636141)   | Windows | GUI| ✔   | ✔   | -   |  -     |     -     |  -  | ✔ | ✔ |
| CH341A     | [NeoProgrammer 2.2.0.10](https://www.dwdvb.com/neoprogrammer-new-update-v2-2-0-10/)  | Windows | GUI | ✔   | ✔   | ✔   |  ✔      |     -     |  -  | ✔ | ✔ | ✔ | ✔ |
| CH347T     | [ch347-nor-prog](https://github.com/981213/ch347-nor-prog)          | Linux | Console  | ✔   | -   | -   |  -     |     -     |  -  | ✔ | - | - |
| CH347T     | [СH347 HighSpeed pr.v1.40](http://www.yaojiedianzi.com/index.php?m=Product&a=show&id=19)| Windows | GUI | ✔   | ✔   | ✔   |  -     |     -     |  -  | ✔ | ✔ |
| CH347T     | [CH347_GUI_SPI_NOR_Flash_](https://github.com/bigbigmdm/CH347_GUI_SPI_NOR_Flash_programmer)| Linux | GUI | ✔   | -   | -   |  -     |     -     |  -  | ✔ | - | - |
| EZP2019+   | [EZP2019+ Ver. 2.0](https://github.com/acontini/EZP2019)       | Windows | GUI| ✔   | ✔   | ✔   |  -     |     -     |  -  | ✔ | ✔ | ✔ |

`✔` - yes.

`-`  - no.

`+/-` - is working, but errors have been detected.
