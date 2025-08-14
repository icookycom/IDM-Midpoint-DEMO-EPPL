<img src="./Docker_IDM_Midpoint_DEMO_EPPL_.png" border="0"></img><br>
<br><br>
:warning: Don't forget to run the Reindex Repository Object in ADMINISTRATION\About on first administartor login, after first start of Docker Compose.
<br><br>
Midpoint<br>
http://localhost:8080<br>
Username: administrator<br>
Password: Test5ecr3t<br>
<br>
Username: *Any User*<br>
Password: Password123<br>
<br>
phpLDAPadmin<br>
http://localhost:8081<br>
Login DN: cn=admin,dc=example,dc=com<br>
Password: Test5ecr3t<br>
<br>
<br>
<b>Docker Compose</b><br>
For the Docker Compose, the Docker environment(Docker Desktop) is required and Internet connection on first run.<br>
<br>
<b>Linux</b><br>
Copy folder IDM_Midpoint_DEMO_EPPL<br>
Start Docker Desktop<br>
./IDM_Midpoint_DEMO_EPPL/docker compose up -d<br>
To turn off<br>
./IDM_Midpoint_DEMO_EPPL/docker compose down<br>
Tu turn off and delete any changes<br>
./IDM_Midpoint_DEMO_EPPL/docker compose down -v
<b><br><br>
<b>Windows</b><br>
<br>
IDM Midpoint EPPL | 1. Docker Compose first run<br>
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/_Vm4GSTNzGE/0.jpg)](https://www.youtube.com/watch?v=_Vm4GSTNzGE)
<br><br>

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

<b>Under Development</b><br>
EPPL 1.02 01.09.25<br>
- Added Manager delegation of Manager status of Department<br>
- Improved Forward Role inhereted role assignment inducement mechanism<br>
- Improved Forward Role role link, no more writing from object Temlate only from assignments<br>
- Improved Departament manager-subordinate mechanism<br>
- Improved Person-Employment Role main employment to organization mechanism<br>
