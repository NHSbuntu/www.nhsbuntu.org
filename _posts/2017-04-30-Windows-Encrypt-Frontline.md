---
title: Managing Windows Encryption -Views from the Frontline
categories: encryption frontline
author_staff_member: kenny-kennington
comments: true
---

I am very proud to have been included in the NHSbuntu Core Team, and wanted to highlight one of the reasons why we believe that this can make a substantial change to the way the NHS spends its money on Software, which is often a hidden cost, because we have to have software to manage our patient information and that information has to be protected (See Data Protection 7th Principle). So how is this managed across an estate as large as the NHS?

Please Welcome Microsoft Bitlocker:
Included in Windows since Vista, but only in Enterprise and Ultimate editions. This was initially covered under the NHS Enterprise Wide Agreement, and in 2008, when Bitlocker was introduced, this wasn't a problem! I was at one of the first organisations to adopt Bitlocker with Windows Vista Enterprise edition, and worked closely with Microsoft to implement this across the entire estate, which then was approximately 3,500 PCs. This did not include GP practices at the time, as there were legacy applications that would not work with Vista so XP remained the OS of choice in Primary Care, and where there were laptops that required XP with Encryption McAfee Safeboot, was being used. However, this caused many problems with staff forgetting the Safeboot key, and there was a cost, so the journey toward encryption costs begins. I moved into IT management in the same year, 2008, so became directly responsible for managing these costs in the organisation.

Fast forward to 2010 - [NHS decides not to renew the EWA](https://www.theregister.co.uk/2010/07/15/nhs_microsoft/). If you read the article in the Register, I can now admit to the fact that I was probably the Anonymous PCT representative, and that 2010 marked my steep learning curve into the complexities of Microsoft licensing! This included, and still does today, reports to what was Connecting for Health (Who employed a licensing specialist to assist with this complex area, whom I got to know well, and still work with today (Thanks Andrea, you know who you are)! We are still submitting reports to NHS Digital on the usage of the EWA licenses, and do so yearly! I expect many studies have been carried out, or not, to establish the true costs of this decision, but we are where we are, so what does this all mean for encryption?

There are many methods for managing and purchasing Microsoft licenses. The general advice we received following the demise of the NHS EWA, was not to purchase anything that wasn't covered under the licensing the NHS retained in perpetuity. However, Enterprise editions of said software was not covered for new devices, and if you wanted to retain the use of Bitlocker for encryption you had to purchase an upgrade license, linked to the OEM license for each new device. This cost ranges depending where you are in the renewal cycle of whichever product you are using to purchase licenses. Currently, for our organisation, which chose not to purchase an Enterprise Agreement (EA) or an Enterprise Subscription Agreement (ESA), and we purchase via a Government fixed price Microsoft Select Agreement, since replaced with the Microsoft Products and Services Agreement (MPSA). This means that for every new PC we purchase, if we want to continue with the elements of an Enterprise edition of Windows, we need an upgrade license.

Bitlocker was introduced as standard in Windows 8 and 8.1, but this wasn't widely adopted in the NHS, so we remained with Windows 7 and the Core Client access licenses (CORECALS) we already had. Windows 10 also includes Bitlocker as standard, and introduces new features, such as Bitlocker to Go, but you still need to manage the encryption keys. You can use Microsoft Bitlocker Administration and Monitoring (MBAM), but you have to license your entire estate with either an EA or an ESA to have access to this tool. You could use an alternative, such as Sophos Endpoint, which is our choice, but there is still a cost involved!

Hardware has come down a lot in price, but consider the licenses we have to layer on top of said cheaper hardware, in order that we can utilise that equipment in our largely Windows Active Directory infrastructures. Which I have broken down below as an example, using prices under an MPSA:

* Join a PC to an Active Directory environment - Requirements - Windows Server CAL  £25
* Encrypt said PC with Bitlocker on Windows 7 - Requirements - Enterprise Upgrade license £190
* Access a MSoft SQL database from said PC - Requirements - SQL CAL - around £136
* Access a Sharepoint Farm from said PC - Requirements - SQL CAL, as above, and a Sharepoint CAL £80
* Use Enterprise features of a Sharepoint Farm, SQL CAL and a Sharepoint Enterprise CAL £70

You can see how the costs begin to mount!

There are alternatives to individual client access licenses, so lets take one, Microsoft SQL Server. Licenses for SQL server are on a per core basis, which can only be bought in pairs. If you want to license your SQL server across the Enterprise and expose it to the web, which negates the requirement for individual SQL CALS, the current costs are: Enterprise Edition of SQL with 1 processor and 4 cores = *£30,000* . More than one processor? Double the cost, and that is only 1 server!!!

If the NHS is going to save any money, we have to look at the alternatives and even that will not negate the requirement to license devices in some form, but the costs will be massively reduced, even if only for encryption of your PC hardware!

How? With NHSbuntu.
