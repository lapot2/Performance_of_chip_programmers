# Performance_of_chip_programmers

## SPI operations time. Testing chip: Winbond 25Q32 (4M)

| Hardware   |       Software          |  Platform  |  User Interface  | Reading | Erasing |  Writing | Data checking | Full Cycle Time |
| :---       |       :---              |     :---   |      :---        | :---: | :---: | :---: | :---: | :---: |
| Raccoon    | Raccoon Flash Explorer Full | Windows, Linux, Android, TV-OS, EFI-Shell | GUI, Console |  5.5-8.0s  |  Auto when In-Write, 0.0s  |  20.0-23.0s   |   Auto when In-Write/In-Read, 0.0s   | 25.5s |
| Raccoon    | Raccoon Demo/Free version  | Windows, Linux, Android, TV-OS, EFI-Shell | GUI, Console |  14.0s  |  Auto when In-Write, 0.0s  |  24.0s   |   14.0s   | 52.0s |
| CH341A     | IMSProg v1.4.3           | Linux   | GUI      | 33.9s  | 12.7s | 328.5s | 33.9s   | 409s |
| CH341A     | SNANDer v.1.7.8          | Linux   | Console  | 33.0s  | 8.0s  | 327.0s | 33.0s   | 401s |
| CH341A     | flashrom v1.2            | Linux   | Console  | 34.6s  | 83.2s | 132.7s | 34.5s   | 285s |
| CH341A     | Ch341 Programmer 1.34    | Windows | GUI      | 36.4s  | 9.0s  | 231.4s | 36.4s   | 313s |
| CH341A     | NeoProgrammer 2.2.0.10   | Windows | GUI      | 36.7s  | 9.1s  | 220.8s | 36.7s   | 303s |
| CH347T	   | ch347-nor-prog	          | Linux   | Console  | 1.1s	  | 0.1s	| 28.9s	 | 1.1s    | 31.2s |
| CH347T	   | CH347_GUI_SPI_NOR_Flash_	| Linux   | GUI	     | 1.6s	  | 9.9s	| 35.0s	 | 13.1s   | 59.6s |
| CH347T	   | СH347 HighSpeed pr.v1.40	| Windows | GUI	     | 0.7s	  | 10.0s	| 8.1s	 | 0.7s    | 18.8s |
| EZP2019+   | EZP2019+ Ver. 2.0        | Windows | GUI      | 33.0s  | 10.4s | 38.7s  | 33.0s   | 115s |
| --------   | Otneh Hi-End Programmers | ------- | ---      | -----  | ----- | -----  | -----   | -----|
| Successor  | 16.3.9163.5055           | Windows | GUI      | 4.8s   | 14.2s | 12.9s  | 4.8s    | 36.7s |
| T48        | Xgpro 12.67              | Windows | GUI      | 1.4s   | 5.1s  | 13.4s  | 1.5s    | 21.4s |
| T56        | Xgpro 12.88              | Windows | GUI      | 0.9s   | 10.9s | 9.1s   | 0.9s    | 21.8s |
| T76        | Xgpro 12.89              | Windows | GUI      | 0.5s   | 11.3s | 16.2s  | 0.5s    | 28.5s |
| RT809H     | 20241125                 | Windows | GUI      | 2.5s   | 10.7s | 19.6s  | 2.5s    | 35.3s |

> At the end of this table, for clarity, the speed of some high-end programmers is also given. But those devices provide completely different capabilities and for a different price tag. Therefore, comparing other parameters is incorrect, and they are not included in other tables.

## Programmer Hardware features

| Hardware   |       Software             |  1.8V Chip support |  Test Clip Support | Overload Protect | Flipped chip protect |  Pins connect checking |  Logic Levels check |  Bus Error check |
| :---       |       :---                 |             :---:  |             :---:  |          :---:   |              :---:   |   :---:                |              :---:  |           :---:  |
| Raccoon    | Raccoon Flash Explorer     | ✔                 | ✔ | ✔ | ✔ | ✔ | ✔ | ✔ |
| Raccoon    | Raccoon Demo/Free version  | easy to add       | ++/- | - | - | - | - | - |
| CH341A     | IMSProg v1.4.3             | Need Adapter      | +/-- | - | - | - | - | - |
| CH341A     | SNANDer v.1.7.8            | Need Adapter      | +/-- | - | - | - | - | - |
| CH341A     | flashrom v1.2              | Need Adapter      | +/-- | - | - | - | - | - |
| CH341A     | Ch341 Programmer 1.34      | Need Adapter      | +/-- | - | - | - | - | - |
| CH341A     | NeoProgrammer 2.2.0.10     | Need Adapter      | +/-- | - | - | - | - | - |
| CH347T	   | ch347-nor-prog	            | +/- Need Adapter  | +/-- | - | - | - | - | - |
| CH347T	   | CH347_GUI_SPI_NOR_Flash_	  | +/- Need Adapter  | +/-- | - | - | - | - | - |
| CH347T	   | СH347 HighSpeed pr.v1.40	  | +/- Need Adapter  | +/-- | - | - | - | - | - |
| EZP2019+   | EZP2019+ Ver. 2.0          | Need Adapter      | +/-- | - | - | - | - | - |

> "Test Clip Support" means providing a set of measures that improve the operation and provide protection against electrical damage to both the programmer and the device being flashed, and if operation is impossible, display more detailed information about a specific problem with the in-circuit connection.

> In-circuit firmware cannot be guaranteed 100% by any of the existing programmers in the world, even those not included in this table, if the target motherboard being flashed does not officially support in-circuit firmware.

## Programmmer software features

| Hardware   | Software                |  Platform  |  User Inter-face  |  SPI | I2C | MW | Edit SR | Extended Chip Parameters search in SFDP | Security area view | Hot Edit IC in External Software|
| :---       |       :---              |     :---   |      :---        |:---:|:---:|:---:| :---:  |   :---:   |   :---:   |:---:|
| Raccoon    | [Raccoon Flash Explorer ](https://t.me/racc00n_news)       | Windows, Linux, Android, TV-OS | GUI, CMD | ✔   | ✔   | -   |  ✔     |     ✔     |  -  | ✔ |
| Raccoon    | [Raccoon Demo/Free version](https://github.com/lapot2/Raccoon-Flash-Explorer-Demo)       | Windows, Linux, Android, TV-OS | GUI, CMD | ✔   | ✔   | -   |  -     |     ✔     |  -  | ✔ |
| CH341A     | [IMSProg v1.3.1](https://github.com/bigbigmdm/IMSProg)         | Linux | GUI  | ✔   | ✔   | ✔   |  ✔     |     -    |  -  | - |
| CH341A     | [SNANDer v.1.7.8](https://github.com/McMCCRU/SNANDer)         | Linux | CMD  | ✔   |+/-  |+/-  |  -     |     -     |  -  | - |
| CH341A     | [flashrom v1.2](https://flashrom.org/)           | Linux | CMD  | ✔   | -   | -   |  -     |     -     |  -  | - |
| CH341A     | [Ch341 Programmer 1.34](https://github.com/YTEC-info/CH341A-Softwares/blob/main/Programas/Windows/CH341Programmer/CH341Programmer%20V1.38/Ch341Programmer.exe?ysclid=ls2wxkusch126636141)   | Windows | GUI| ✔   | ✔   | -   |  -     |     -     |  -  |
| CH341A     | [NeoProgrammer 2.2.0.10](https://www.dwdvb.com/neoprogrammer-new-update-v2-2-0-10/)  | Windows | GUI | ✔   | ✔   | ✔   |  ✔      |     -     |  -  | - |
| CH347T     | [ch347-nor-prog](https://github.com/981213/ch347-nor-prog)          | Linux | CMD  | ✔   | -   | -   |  -     |     -     |  -  | - |
| CH347T     | [СH347 HighSpeed pr.v1.40](http://www.yaojiedianzi.com/index.php?m=Product&a=show&id=19)| Windows | GUI | ✔   | ✔   | ✔   |  -     |     -     |  -  |
| CH347T     | [CH347_GUI_SPI_NOR_Flash_](https://github.com/bigbigmdm/CH347_GUI_SPI_NOR_Flash_programmer)| Linux | GUI | ✔   | -   | -   |  -     |     -     |  -  | - |
| EZP2019+   | [EZP2019+ Ver. 2.0](https://github.com/acontini/EZP2019)       | Windows | GUI| ✔   | ✔   | ✔   |  -     |     -     |  -  | - |

> `✔` - yes.
>
> `-`  - no.
>
> `++/-` - It will most likely work.
>
> `+/--` - It's unlikely to work.
>
> `+/-` - is working, but errors have been detected.
>
> `SFDP` is a special flash memory chip register that stores data about the chip for automatic support of this chip by various devices, including flash memory programmers, without the need to add chip parameters to the database or manually set the parameters.
>
> Despite the mandatory presence of this information in the chip since 2011, most memory chip programmers use only databases, or use the information built into the chip very limitedly.

