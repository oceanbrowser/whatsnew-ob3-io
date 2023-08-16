# OB3 S2 2023 updates 

Latest update: August 16th 2023

### Support enhancement - Intercom - email users who only login once after seven days

- sent after 7 days if the user has only one session in OB3.  This message is just to ensure that user did not have a problem logging in or accessing their course content 
- message sent via email

![image-20230816165755816](index.assets/image-20230816165755816.png)

### Temporarily disable legals acceptance screen

- disabled the legals acceptance screen while we undertake additional testing of this UX screen.  Will be reenabled in our next update.  When reenabled any new users who have not been prompted to accept terms will see screen on next login.

### Edit and Share enhancements for instructors

- when sharing a course via LTI the default privilege for Instructors (teachers) is Edit and Share.  This privilege will allow teachers to modify sharing on content within a course without having to access the PMA (Dept) account where course sharing is setup.  
  - The intention of this privilege is to allow the OB3 co-ordinator (or trained staff within a Department) to undertake OB3 course rollovers and setup, while allowing teachers to be able to modify course sharing on content without having to have access to the PMA (Departmental) account.
  
- Today's enhancement improves the teacher UX for Edit and Share by:
  - preventing Instructors from (typically accidentally) deleting Learner or Instructor groups, which are required for correct LTI course sharing operation, from their teacher account.  These groups now appear without the "x" delete option. 
  - hide groups which cannot be configured by the teacher from their account. Teachers must use the PMA account if they wish to adjust LTI course groups.  This means a teacher may sometimes see that a course has 3 groups but when viewing the course the groups may not appear.  If groups are not visible in the sharing dialog, this means they need to be edited in the PMA account.
  - Teachers can modify sharing within the course - for example allowing a student to have edit rights on a document or folder.  Teachers can create their own groups and use with course sharing. This provides the flexibility required for various collaborative activities and portfolio cases of use that OB3 supports.

### Release notes website

- added this release notes (what's new) website, where details of OB3 updates will be posted.

### Bug fixes

- when using OB3 clipboard if you cut and paste feature to move content within the same document sometimes pasted content would sometimes appear in wrong position. 

  ![image-20230815124817911](index.assets/image-20230815124817911.png)

- you can use the link button in the OB3 sidebar to obtain a URL pointing to specific content in a document (for example a specific discussion or heading, ie a deep link).  Fixed a bug where this UX element would not hide after use. 

- update cut paste logic when used to cut a list item (or items) from within a list and paste as paragraph.  Previously would "alias" the pasted paragraph instead of pasting it which we do not support.

### Sharing and Permissions design update

![image-20230815130213971](index.assets/image-20230815130213971.png)

- updated the design of the Sharing and permission dialog.  This now appears as a modal window. 
- added a red close button at top right to visually distinguish from the sharing privileges - this is to help prevent users from accidentally deleting shares when trying to close dialog
- added button bar at bottom including a new Help button that goes to sharing topics on guide.ob3.io website.  Additional help articles will be posted there

### Updates to LTI course sharing

- previously when sharing a course to LTI only one gruop was added to the sharing dialog (the LTI course group).  Now we add three groups, the course group, the instructor and the learner group.  This ensures that teachers can view learner and instructor details easily by clicking the hyperlinks on the corresponding group to view membership.  It also ensures that privileges set are more explicitly visible
- disable LTI will remove the LTI parent group and prevent new users joining the course, but teacher must manually delete learner and instructor group if access to existing users to be disabled.  This allows alumni to continue to access course content.

### Record Instructor status and Department (Programme) on LTI launch

- updated OB3 intercom to record the Department a user is studying in when user joins a course via LTI.  This enables clients to request a per-department breakdown of users who have joined courses via LTI.  Note we typically only retain intercom active users for 45 days, so this will provide a breakdown of users active in the last 45 days.

- record whether user is an instructor.  This tag will be used to provide instructor onboarding campaign to introduce teachers progressively to OB3.  Topics will be added to guide.ob3.io website and introduced to teachers through Intercom email and in-app messages.

### Table editing update

![image-20230815144844566](index.assets/image-20230815144844566.png)

- updated Table editing commands to visually separate (with divider lines)  Remove options from Insert operations.  This is to further help users avoid accidentally deleting column elements when they don't intend this

### Azure post-migration updates

- system updates to OB3 after our first week in operation on Azure Cloud

### Bug fixes

- fixed a bug in video and audio transcoding to ensure that we don't check uploads in progress that are more than 7 day.

- fixed a bug in the password reset screen
- updated Slack logging to ensure only critical logging events are sent to slack
- updates to logging and monitoring
- forbid operations that would ever add a component into itself

# Major update: OB3 Azure Cloud release

- this update deployed on Sunday July 2nd
- OB3 code base has been restructureded into packages, in preparation for supporting the next major OB3 feature release
- Migrate OB3 Cloud files to Sydney region
- OB3 data and services migrated to Sydney Australia data region
- OB3 delivered as a containerised (docker) application running under Azure App Service and Azure Cassandra as Managed Service database
- improvements to application monitoring and logging
- security enhancements
- application performance and scalability enhancements
- improvement resilience, with easy ability to deploy OB3 in different geographical regions, or to support dedicated OB3 instances for Enterprise customers
- improved developer workflows allowing faster release of enhancements and updates
- migrate OB3 custom elearn apps such as the Virtual Ophthalmic Clinic web app to Azure and deployed in Sydney region

# OB3 S1 2023 Updates

Check back later for further updates in this section

### Table Deletion warnings

- Student portfolios in OB3 use tables extensively.  These enhancements are designed to help students avoid accidentally deleting tables or columns
- show warning dialog and ask user to confirm when attempting to delete a table with many cells.  
- show warning dialog and ask user to confirm when user attempts to delete a column from a table containing many cells.  

### Add keyboard command support for common document editing operations

![image-20230816133302744](index.assets/image-20230816133302744.png)

- add support for changing style of paragraphs from keyboard.  
- add support for changing paragraph to list (option + L) or table (option + T) from keyboard.  The list command is particularly helpful when using lists extensively
- update OB3 keyboard help map (accessible via the keyboard icon at the bottom right of OB3)

### Update Copy to Clipboard features

- Update "Copy to clipboard" buttons throughout OB3 to use modern browser copy methods.  Buttons now correctly copy content (such as URLs) to clipboard

### Remove Flash support

- remove legacy code from OB3 (and OB3 application build processes) related to supporting Flash content.  Please note if you have educational content that uses Flash we are able to support this using the Ruffle flash player.  Please contact help@ob3.io for assistance

### Preparing OB3 for deploying to the Azure Cloud

- tasks ongoing over the last year (2022-23) and are too extensive to list here
- extensive testing in Azure App service since November 2022
- testing and documentation of application migration process
- development and updating of operations documentation

### Set document name when navigating OB3 content

![image-20230816133910682](index.assets/image-20230816133910682.png)

- when navigating OB3 content change the browser window title to match the content being viewed.  Supports updates for navigating courses and folders, and for documents opened.
- Note that by recording this inforrmation browser history will now show your navigation through OB3 content allowing students to return to content they have previously viewed (note: if using Chrome Incognito window you may need to re-enable history recording which is disabled by default)

### Add Privacy Policy and Terms of Service acceptance screen

![image-20230816134713679](index.assets/image-20230816134713679.png)

- add startup screen for new users to view and accept terms of service and privacy policy agreements

### Enterprise customer updates

- a number of tasks were completed for enterprise customers in this period, details ommitted here for client privacy reasons

### Miscellaneous updates

- update wording on OB3 new account activation email - sent to users who are invited to OB3 via email
- update OB3 password reset policy to reject passwords that are too insecure
- update code for detecting Grammerly browser extension and disabling in OB3.  OB3 (in common with many other editing apps) does not support Grammarly as it interferes with content editing.
- disable pasting images or file attachments into lists or tables
- update database connection logic to more reliably handle database socket connection timeouts