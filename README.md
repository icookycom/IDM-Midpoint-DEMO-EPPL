IDM Midpoint DEMO EPPL<br>
Employments Positions Projects LDAP<br>
<br>
Version:<br>
<b>EPPL 1.01 18.07.25</b><br>
Compatibility: Evolveum midPoint 4.9.1<br>
Incompatible: Evolveum midPoint 4.9.2,4.9.3 - due to Evolveum BUG for Person of interest filters in GUI Request access<br>
<b>Changes with Respect To Version EPPL 1.0 30.06.25</b><br>
- Added Login Stop List<br>
- Added Infinitely Logins (numbers are added to the end of the login)<br>
- Added Head Department inherits Company Name<br>
- Added personalNumber in Search Box of views All Users, My IDM Subordinates, All Account Users, Employment Users, Position Users<br>
- Added filter "Dep.Managers only" in Search Box of view Position Users<br>
- Faster first Reconcilation in some Resources with Multi-node<br>
- Improved Task "EPPL delete nickName without members" for "Login Stop List"<br>
- Impoved Login/nickName generation Script for "Login Stop List" and "Infinitely Logins"<br>
- Moved from view Persons to view All Account Users in Search Box "Users with account" and "Users without account"<br>
- Fixed EPPL RED Error: GUI Boss Request LDAP account to own Position<br>
- Fixed EPPL All Account Users name in Search Box Object Collection list<br>
- Changed the color and text of the warning "not authorized for operation" to avoid scaring employees in their GUI<br>
- ...other last minute changes<br>

<br>
<b>Docker</b><br>
Compose <a href="https://github.com/icookycom/IDM-Midpoint-DEMO-EPPL/tree/main/Docker">IDM-Midpoint-DEMO-EPPL/tree/main/Docker</a><br>
<br>
<b>Storytelling EPPL 1.0</b><br>
<a href="https://habr.com/ru/articles/923278/">Docker Demo IDM Midpoint EPPL c трудоустройствами, назначениями, проектами и LDAP</a><br>
<br>
<b>Schema EPPL 1.01</b><br>
<img src="https://github.com/icookycom/IDM-Midpoint-DEMO-EPPL/blob/main/Schema%20IDM%20MIdpoint%20EPPL.png" border="0"></img><br>
<br>


<b>EPPL Functionality</b><br>
<b>1. Employments</b><br>
Creation/blocking from HR source<br>
Linking to an employee from HR source<br>
Creating assignment roles from employment roles<br>
Creating system accounts for employment<br>
<b>2. Positions</b><br>
Creation/blocking from HR source<br>
Linking to employment from HR source<br>
Requesting assignment roles<br>
Creating system accounts for assignments<br>
<b>3. Projects</b><br>
Project creation and editing by employees with project creation rights<br>
Adding/removing project members<br>
Adding/removing project rights<br>
Creating custom project roles<br>
Assigning custom project roles to a project member or to the project itself<br>
Revoking custom project roles when a member is removed from the project<br>
Disabling a project and removing all its members<br>
<b>4. SOD (Segregation of Duties)</b><br>
Role assignment approval workflows<br>
Restrictions on role acquisition based on recipient type and company affiliation<br>
<b>5. Subordinates</b><br>
Requesting access rights for subordinates<br>
Viewing a subordinate’s photo<br>
Hierarchical determination of supervisors by department<br>
<b>6. Login/nickName Generation</b><br>
Cyrillic is converted to Latin<br>
Generated at the time of account assignment<br>
Uniqueness is checked against the name in Midpoint and cached resources data<br>
Updated when the last name changes in the HR source<br>
Login is released if no accounts are associated<br>
Login Stop list (EPPL 1.01)<br>
Infinitely Logins (EPPL 1.01)<br>
<b>7. Personal Data</b><br>
Viewing restrictions<br>
<b>8. Connected Resources</b><br>
LDAP accounts/groups<br>
MS AD (Active Directory) accounts/groups<br>
Creating Forward Roles from LDAP groups<br>
Creating Forward Roles from MS AD groups<br>
Creating Personal Data<br>
Exporting photos to LDAP<br>
Creating Employees/Employments/Assignments from HR sources (multiple resources)<br>
<b>9. Company</b><br>
Company Name propagates to Role Catalog Head, Departmen Catalog Head(EPPL 1.01), Employments, Popsitions<br>
<br>
<b>Data</b><br>
EPPL pulls HR data from a CSV file using the CSV Connector, but this can easily be adapted to use a DB connector instead. All the data is stored in the file EPPL_HR_DATA.csv, located at /opt/midpoint/var/info.<br>
<img src="https://github.com/icookycom/IDM-Midpoint-DEMO-EPPL/blob/main/DEMO%20IDM%20Midpoint%20EPPL%20DATA.png" border="0"></img><br>
Main Fields
- **`number_eppl`** – Unique sequential number.  
- **`type_eppl`** – Record type.  
- **`main_id`** – Unique identifier:  
  - For **User (employee)**: HR ID.  
  - Assignments start with `POS`, employments with `EMP`.  
- **`parent_id`** – Organization code (from `ADMINISTRATION/Roles/Company Roles`).  
- **`member_of_eppel`** – Associated entity (singular, used for `association` in the resource).  
- **`department_eppl`** – Department code for the assignment (from `ADMINISTRATION/Org.structure/Department Catalogs`).  
- **`department_relation_eppl`** – If `manager`, denotes department head; otherwise empty.  
- **`status_eppl`** – Status: set this to `disabled` to revoke assignment/employment.

Remaining fields contain supplementary information.<br>
<br>
<b>Video Steps</b><br>
<a href="https://www.youtube.com/@IDMMidpointEPP">www.youtube.com/@IDMMidpointEPPL</a><br>
<br>
IDM Midpoint EPPL | 1. Docker Compose first run<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/_Vm4GSTNzGE/0.jpg)](https://www.youtube.com/watch?v=_Vm4GSTNzGE)
<br>
IDM Midpoint EPPL | 2. Admin logon and LDAP setup<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/9LUTxprl0qQ/0.jpg)](https://www.youtube.com/watch?v=9LUTxprl0qQ)
<br>
IDM Midpoint EPPL | 3. Users Employments Positions Data from HR CSV File<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/_-rb96uvJsQ/0.jpg)](https://www.youtube.com/watch?v=_-rb96uvJsQ)
<br>
IDM Midpoint EPPL | 4. GUI User Boss Request access for Position, Roles LDAP Group & Account<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/0BuCAcwSCX8/0.jpg)](https://www.youtube.com/watch?v=0BuCAcwSCX8)
<br>
IDM Midpoint EPPL | 5. GUI User Request Access Role with approval Role with SOD<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/DbhlUrv10wg/0.jpg)](https://www.youtube.com/watch?v=DbhlUrv10wg)
<br>
IDM Midpoint EPPL | 6. GUI User: Project Creation and Management it Roles, Members, Status<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/NTscJCasI_U/0.jpg)](https://www.youtube.com/watch?v=NTscJCasI_U)
<br>
IDM Midpoint EPPL | 7. GUI User Managing dedicated Project Roles<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/u7g0Neyn3rE/0.jpg)](https://www.youtube.com/watch?v=u7g0Neyn3rE)
<br>
IDM Midpoint EPPL | 8. Dismissal from Position, Multiple Accounts, Users photo to LDAP<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/fCVq6cfEKKY/0.jpg)](https://www.youtube.com/watch?v=fCVq6cfEKKY)
