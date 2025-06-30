<img src="./Docker_IDM_Midpoint_DEMO_EPPL_.png" border="0"></img><br>
<br>
Midpoint<br>
http://localhost:8080/midpoint/<br>
Username: administrator<br>
Password: Test5ecr3t<br>
<br>
phpLDAPadmin<br>
http://localhost:8081<br>
Login DN: cn=admin,dc=example,dc=com<br>
Password: Test5ecr3t<br>
<br>
<br>
<br>
<b>Docker Compose</b><br>
For the Docker Compose, the Docker environment is required and Internet connection on first run.<br>
<br>
<b>Linux</b><br>
Copy folder IDM_Midpoint_DEMO_EPPL<br>
To start<br>
./IDM_Midpoint_DEMO_EPPL/docker compose up -d<br>
To turn off<br>
./IDM_Midpoint_DEMO_EPPL/docker compose down<br>
Tu turn off and delete any changes<br>
./IDM_Midpoint_DEMO_EPPL/docker compose down -v
