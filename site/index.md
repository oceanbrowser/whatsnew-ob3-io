# OB3 Release notes - 2023

## August 14th

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

## August 7th

### Sharing and Permissions design update

![image-20230815130213971](index.assets/image-20230815130213971.png)

- updated the design of the Sharing and permission dialog.  This now appears as a modal window. 
- dded a red close button at top right to visually distinguish from the sharing privileges - this is to help prevent users from accidentally deleting shares when trying to close dialog
- added button bar at bottom including a new Help button that goes to sharing topics on guide.ob3.io website.  Additional help articles will be posted there