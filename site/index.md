# OB3 S2 2023 updates 

## August updates

### Edit and Share enhancements for instructors

- when sharing a course via LTI the default privilege for Instructors (teachers) is Edit and Share.  This privilege will allow teachers to modify sharing on content within a course without having to access the PMA (Dept) account where course sharing is setup.  Today's enhancement changes how Edit and Share works by 
  - preventing Instructors from (typically accidentally) deleting Learner or Instructor groups, which are required for correct LTI course sharing operation, from their teacher account.  These groups now appear without the "x" delete option. 
  - hide groups which cannot be configured by the teacher from their account. Teachers must use the PMA account if they wish to adjust LTI course groups.  
  - Teachers can modify sharing within the course - for example allowing a student to have edit rights on a document or folder.  This provides the flexibility required for various collaborative activities and portfolio cases of use that OB3 supports

### Release notes website

- added this release notes (what's new) website, where details of OB3 updates will be posted.

### Bug fixes

- when using OB3 clipboard if you cut and paste feature to move content within the same document sometimes pasted content would sometimes appear in wrong position. 

  ![image-20230815124817911](index.assets/image-20230815124817911.png)

- you can use the link button in the OB3 sidebar to obtain a URL pointing to specific content in a document (for example a specific discussion or heading, ie a deep link).  Fixed a bug where this UX element would not hide after use. 

### Sharing and Permissions design update

![image-20230815130213971](index.assets/image-20230815130213971.png)

- updated the design of the Sharing and permission dialog.  This now appears as a modal window. 
- added a red close button at top right to visually distinguish from the sharing privileges - this is to help prevent users from accidentally deleting shares when trying to close dialog
- added button bar at bottom including a new Help button that goes to sharing topics on guide.ob3.io website.  Additional help articles will be posted there

## July Updates

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

Details to come