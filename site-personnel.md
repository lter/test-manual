# Site Personnel Lists 

> [!NOTE] 
> SalesForce database has been deprecated. Personnel reporting continues in Google sheets for now, but is moving to the lternet website. Email Marty for permission to edit google sheets if you don't have it.test

## Overview

Rather than having an individual simply associated with a site or not, we strive to maintain a record of prior associations and allow multiple simultaneous associations (with different sites, in different roles, and with different institutions) for individuals. This is valuable for understanding how individuals interact with the Network across their careers. To accomplish it, however, we need to update **affiliations**, (a record of person-site-role-time period) rather than just people's current affiliation with a site.

## Making bulk updates **(new July 27, 2024)**

Usually, there are a few times a year when many people need to be added at once. Edits to LTER site personnel can be made directly in [the LTERHub-ex-im google sheets document](https://docs.google.com/spreadsheets/d/1TSmzt-Cg2xIKlJ3uin8EoMclACThkPiWqwroG3JoPdQ/edit#gid=293749749). Lead site information managers and designated updaters for each site have read access to the file. Edit permissions will be granted on a sheet-by-sheet basis to one designated updater per site.
   
> [!NOTE]
> Note that Google sheets, unlike Excel sheets or csv files, save data continuously as they are entered.*

### Overall workflow ###
-  Each site has its own tab in the spreadsheet. Before you plan to make edits, please identify one editor per site and request file edit access for them by emailing Marty. 
-  Using the instructions below, make edits to your site's personnel list. Where you do not have changes to make, simply leave the the existing information.
-  Add new individuals and new affiliations to the bottom of the list, leaving the SalesForce ID columns blank
-  **IMPORTANT: Notify Marty when you have made a batch of updates**

### Individual Updates ###
For the moment, we are focused on bulk updates. The LNO will announce a new process (and training) for individual updates in the near future.

> [!NOTE]  
> The API function was part of SalesForce and was rarely used. It has been deprecated temporarily. Once the transition to website updating is complete, we can re-establish it.

## Row and Column Descriptions ##

#### Rows ####

-  **Row 1** is blank
-  **Row 2** lists the common-language descriptions of each field. 
-  **Row 3** lists the SalesForce names for each field. This assists in upload and should not be edited.   
-  **Data rows:** Each data row represents an **affiliation** between an individual and a site in a particular role, for a specific period of time. Thus, an individual may appear in multiple rows with different roles. Within each sheet, records are sorted first by "Current" or "Former" status and then alphabetically by last name. Be aware that the same individual may have both current and former affiliations, or may have multiple current affiliations. 

#### Columns ####

-  **Database Keys:**
   -  A.  **Affiliation ID** *(protected)*: The unique key for the specific affiliation (role-site/institution-individual combination)
   -  B.  **Contact ID** *(protected)*: The unique key for the individual contact associated with that affiliation
   -  C.  **Account ID** *(protected)*: The unique key for the account (site or institution) associated with that affiliation
   -  D.  **Profile ID** *(protected)*: The unique key for the user associated with that affiliation
  
-  **Site Information:**  
   -  E.  **Acronym**: The 3-letter site acronym. This should **always** match the spreadsheet tab in which you are editing. If an affiliation with a different site needs to be created or edited, that should be done by the individual or by the designated editor for that site.
   
-  **Contact-related information:**  	
   -  F.  **Last Name**: Last name of the individual contact. Text fields can accept both hyphenated and un-hyphenated names. Special characters may be used with caution, but HTML formatting is not permitted. 
   -  G.  **First Name**: First name of the individual contact	
   -  H.  **Middle Name**: Middle name or initial of the individual contact (if known). If initials are used, please include a period.
   -  I.  **Email**: Active email address of the individual contact. Be cautious in changing this. It also serves as the user's login and (especially for former site participants) you may not have the most current information.	
   -  J.  **ORCID**: Once entered, this is unlikely to change.	Users will be prompted to update ORCIDs on site registration.
   -  P.  **Contact-Site ID**: If your site uses a unique identifier for individuals that could aid in matching site and network-level information, this is the place to enter it. If you do not use such a system, please leave this field blank.	*(Located at the end as only a few sites use this field.)*

-  **Affiliation-related information:**
   -  K.  **Role (Affiliation)**: Recall that participants may have multiple simultaneous affiliations. This field holds the role for one affiliation with a particular site. The (limited) choices for this field are available in the drop down. Please DO NOT add choices that do not appear in the drop down selector. [Options for "Role"](#Detailed-Field-descriptions-and-options) are detailed later on this page.
   -  L.  **Start Year (Affiliation)**: The year that this affiliation started - to the best of your knowledge. This information is not strictly required and participants can update this information directly when they register on the site.
   -  M.  **End Year (Affiliation)**: 	The year that this affiliation ended - to the best of your knowledge. This information is not strictly required and participants can update this information directly when they register on the site. When an entered end year is less than the current year, the affiliation status will be automatically converted to "Former" at the time data is uploaded.
   -  N.  **Status (Affiliation)**: Status" has 2 options: "Current" or "Former." This reflects an individual's affiliation *with the site*. All newly affiliated individuals should be listed as "Current." When an individual leaves your site, they should be identified as "Former" for your site and an end date entered for their role. When their status changes to "Former" at all sites with which they had an affiliation, their LTER status will automatically change to "Inactive". As long as they maintain an active affiliation with any LTER site, their LTER status will be "Active." This field controls whether individuals appear in the site directory for the affiliated site.
   -  O.  **Primary (Affiliation)**: This Boolean field identifies *this* affiliation as the primary one (across all LTER associations) for the associated individual. In general, it should be set by the individual during the registration process. Among several possible affiliations, it will usually be the most active or the most recent.	
 
-  **User-related information:**
   -  Q.  **Active User?**: This field contains a Boolean (true/false) value indicting whether a user has been activated for this contact.
   
-  **Upload/Update results columns**: Columns S and beyond are used to store the result of the most recent uploads to SalesForce. Failures may indicate duplicate names or other conditions that require investigation. They should not be edited except by the LNO. 

### Specific Use Cases ###

*  **New participants:** Add new site participants at the bottom of your site's sheet, below the existing entries. Often, individuals who are new to your site actually have a prior LTER identity. When they are using the same email address, these duplicates will be caught on creation. If they are using a new email address, the LNO will eventually find and resolve them. For new participants with more than one role, include only the primary role at this stage. Follow the instructions below for "adding roles" to add additional affiliations. Fill in:	
   * Last Name 
   * First Name
   * Middle Name (if known) 
   * Email 
   * ORCID (if known): Use the full http format, e.g https://orcid.org/0000-0003-2833-956X
   * Role (with respect to your site): If the individual will hold multiple roles, add them each on a new line.	
   * Start Year (Affiliation): For new individuals, this will typically be the current year.	
   * End Year (Affiliation): For new individuals, leave this blank.
   * Status (Affiliation): Choose "Current"
   * Primary (Affiliation): If you are quite confident that this affiliation is the primary LTER affiliation for this individual, enter TRUE or conversely, FALSE. Otherwise, leave this field blank.
   * Contact-Site ID: If your site uses this field, enter the site-id for the individual. Enter the same site-id for all affiliations that individual may have with your site. If your site doesn't use this field (most sites) leave it blank.	
   * Active User?: **Leave this field blank**
   
*  **Adding roles:** Add new roles at the bottom of your site's sheet, below the existing entries and the new participants. Separate new roles from new participants with a blank line. Copy contact-related information (Last Name, First Name, Middle Name, Email, and ORCID) from an existing affiliation for that individual and update the affiliation-related information as needed.

* **Ending roles:** To end a role for an individual, simply enter the year that they stopped serving in that role into the "End Year (Affiliation)" field. If they never served that role, please contact Marty Downs (downs@nceas.ucsb.edu) for troubleshooting assistance.

* **Former participants:**
> [!WARNING]  
> We are currently resolving an issue with the display of former participants on the [LTER directory](https://lternet.edu/directory/). For the moment, please ensure that the affiliation status in the LTER-ex-im Google sheet is correct and we will resolve the directory display as soon as possible.

Once an individual has left the site, please change their "Status (Affiliation)" field to "Former". If you can make a fair guess at an end year, include that information under "End Year". If you can't guess within a year or two, leave it blank. 

## Detailed Field descriptions and options 

A few fields use limited options and will not accept any text other than the below.

* Site options: AND, ARC, BES, BLE, BNZ, CAP, CCE, CDR, CWT, FCE, GCE, HBR, HFR, JRN, KBS, KNZ, LUQ, MCM, MCR, MSP, NES, NGA, NTL, NWT, PAL, PIE, SBC, SEV, SGS, VCR
    * Special Options: EDI, LNO, INT, NWK are for personnel associated with the Environmental Data Initiative (EDI), LTER Network Office (LNO), International LTER (INT), and the Network as a whole (NWK)--for example, staff of related organizations and networks. 
* Site Role:
    * **Lead Principal Investigator:** The primary individual who is responsible for the scientific or technical direction of the project.
    * **Co-Principal Investigator:** The individuals who are formally responsible for the scientific or technical direction of the project. (Cover page investigators.) 
    * **Investigator:** An individual with substantial scientific involvement in the LTER, but who is not a Co-Principal Investigator(s). LTER Investigators need not be funded by the project.
    * **Postdoctoral Associate:** An individual with a doctoral-level degree who does research at the site, but does not hold a permanent position. Generally Postdocs are less than 5 years post-degree.
    * **Graduate Student:** A part-time or full-time student working on the project in a research capacity who holds at least a bachelor's degree and is enrolled in a degree program leading to an advanced degree.  
    * **Undergraduate Student:** A student working on the project in a research capacity who is enrolled in a degree program (part-time or full-time) leading to a bachelor's or associate's degree. 
    * **Information Manager:** A person at an LTER site that spends some or all of their time in the process of data and information management. This person may or may not be the site representative to the information management committee.
    * **Education Manager:** A person at an LTER site that spends some or all of their time in the process of education/outreach. This person may or may not be the site representative to the education/outreach committee.  
    * **Other Professional:** A person who may or may not hold a doctoral degree or its equivalent, who is considered a professional and is not reported as a Principal Investigator, Co-principal Investigator, Investigator, Postdoctoral Associate or Student. Examples include research associates, physicians, veterinarians, system experts, computer programmers and design engineers.
    * **Technical/Research Staff:** Technicians and field research personnel.
    * **Education/Communications Staff:** Educators or science-focused communicators.
    * **Administrative Staff:** Persons working on the project in a non-research capacity in an administrative role. 
    * **Other Staff:** Persons working on the project in a non-research capacity, such as draftsmen, animal caretakers, electricians and custodial personnel. 
    * **Interested Party:** A person who is associated with an LTER site or the Network through interest, educational programs, public outreach etc., may include educational or community partners, neighbors, board members, etc. 
    * **Retired:** _Emeritus_ Investigators who maintain an active interest in the site and the Network. Not necessarily the same as past network members (who are designated as "Former"). 

* Less-frequently used Site Role options, for individuals that you want to associate with your site in specific roles:
    * K-12 Teacher
    * Volunteer
    * Media
