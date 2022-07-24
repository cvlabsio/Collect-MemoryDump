# Collect-MemoryDump
Collect-MemoryDump - Automated Creation of Windows Memory Snapshots for DFIR

Collect-MemoryDump.ps1 is script utilized to collect a Memory Snapshot from a live Windows system (in a forensically sound manner).

Features:
* Checks for Hostname and Physical Memory Size before starting memory acquisition
* Checks if you have enough free disk space to save memory dump file
* Collects a Raw Physical Memory Dump w/ DumpIt, Magnet RamCapture and WinPMEM
* Collects a Microsoft Crash Dump w/ DumpIt for Comae Beta from Magnet Idea Lab
* Checks for Encrypted Volumes w/ Magnet Forensics Encrypted Disk Detector
* Collects BitLocker Recovery Key
* Checks for installed Endpoint Security Tools (AntiVirus and EDR)
* Enumerates all neccessary information from the target host to enrich your DFIR workflows
* Creates a password-protected Secure Archive Container (PW: IncidentResponse)

## First Public Release    
MAGNET Talks - Frankfurt, Germany (July 27, 2022)  
Presentation Title: Modern Digital Forensics and Incident Response Techniques  
https://www.magnetforensics.com/  

## Download  
Download the latest version of **Collect-MemoryDump** from the [Releases](https://github.com/evild3ad/Collect-MemoryDump/releases/latest) section.  

## Usage  
.\Collect-MemoryDump.ps1 [-Tool] [--skip]

Example 1 - Raw Physical Memory Snapshot  
.\Collect-MemoryDump.ps1 -DumpIt

Example 2 - Microsoft Crash Dump (.zdmp) &#8594; optimized for uploading to [Comae Investigation Platform](https://www.comae.com/)  
.\Collect-MemoryDump.ps1 -Comae  

Note: You can uncompress *.zdmp files generated by DumpIt w/ Z2Dmp (Comae-Toolkit).

![Help-Message](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/01.png)  
**Fig 1:** Help Message  

![AvailableSpace](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/02.png)  
**Fig 2:** Check Available Space

![DumpIt](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/03.png)  
**Fig 3:** Automated Creation of Windows Memory Snapshot w/ DumpIt

![RamCapture](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/04.png)  
**Fig 4:** Automated Creation of Windows Memory Snapshot w/ Magnet RAM Capture

![SkipCompressing](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/05.png)  
**Fig 5:** The time-consuming task of compressing the memory snapshot can be skipped (if needed)  

![WinPMEM](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/06.png)  
**Fig 6:** Automated Creation of Windows Memory Snapshot w/ WinPMEM

![Comae](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/07.png)  
**Fig 7:** Automated Creation of Windows Memory Snapshot w/ DumpIt (Microsoft Crash Dump)

![MessageBox](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/08.png)  
**Fig 8:** Message Box

![SecureArchive](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/09.png)  
**Fig 9:** Secure Archive Container (PW: IncidentResponse) and Logfile.txt

![Directories](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/10.png)  
**Fig 10:** Output Directories

![Memory](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/11.png)  
**Fig 11:** Memory Snapshot (in a forensically sound manner)

![SystemInfo](https://github.com/evild3ad/Collect-MemoryDump/blob/64d99221e407893ec3530550404c6d9c849afdf3/Screenshots/12.png)  
**Fig 12:** System Information

## Links
[Comae-Toolkit incl. DumpIt](https://www.magnetforensics.com/blog/how-to-get-started-with-comae/)  
[MAGNET Ram Capture](https://www.magnetforensics.com/resources/magnet-ram-capture/)  
[WinPMEM](https://github.com/Velocidex/WinPmem)  

![Comae](https://www.comae.com/images/MF_Comae_Acquisition_ComaeWebsite2_1200x675.jpg) 
