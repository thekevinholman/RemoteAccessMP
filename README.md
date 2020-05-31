# Microsoft Windows Server Remote Access Management Pack 10.0.0.10

This MP is an adaptation of the Windows Server 2012R2 Remote Access Management pack.  I made the MP OS version agnostic, which has been tested with Windows Server 2012, 2012R2, 2016, and 2019

10.0.0.0 - Original Release
* Changed the discovery to be OS version agnostic
* Disabled all the event collection rules (what a terrible thing to do originally!)
* Cleaned up the ID of the MP, and some class names

10.0.0.10 - Multiple updates:
* Change the ID of the MP
* Removed the massive number of classes.  They served absolutely no purpose and just bloated the MP.  A very common issue with a lot of Microsoft MP’s.
* Rewrote the Distributed Application to contain Remote Access Servers instead of sites, so it populates now.
* Removed On-Demand detection from the Heuristic monitortype, and set “ConfirmDelivery=false” on all Heuristic monitors, which was breaking cookdown.
* Added a RunAs profile, which will be used by the discovery script and the Heuristics script monitor, if needed.
* Cleaned up the views
* Cleaned up the discovery and monitoring PowerShell scripts
