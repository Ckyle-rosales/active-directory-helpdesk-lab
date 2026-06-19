This project demonstrates a basic Active Directory help desk environment using Windows Server, Windows 10/11 Pro, and VirtualBox. The lab simulates common IT support tasks such as creating users, managing security groups, joining a client computer to a domain, configuring shared folder permissions, resetting passwords, unlocking accounts, and applying Group Policy.

Lab Environment
Virtualization: Oracle VirtualBox
Server: Windows Server
Client: Windows 10/11 Pro
Domain Controller: DC01
Domain: helpdesk.local
Client Computer: CLIENT01
Project Goals
Install and configure a Windows Server domain controller
Create an Active Directory domain
Organize users, groups, and computers using OUs
Join a Windows client computer to the domain
Test domain user logins
Configure shared folder permissions using security groups
Simulate common help desk tasks
Apply a Group Policy login banner
---------------------------------------
Installed VirtualBox and created Windows Sever Virtual Machine named AD-Server-DC01.
<img width="1564" height="783" alt="image" src="https://github.com/user-attachments/assets/d5d63996-2c99-423c-98c4-d7e083e4e009" />

Installed Windows Server Standard Evaluation with Desktop Experience for the Active Directory domain controller.
<img width="1002" height="812" alt="image" src="https://github.com/user-attachments/assets/17cefbdd-38a9-4303-ad0a-dfe75fa39c5f" />

Logged into Windows Server and opened Server Manager to begin configuring the domain controller.
<img width="1008" height="752" alt="image" src="https://github.com/user-attachments/assets/ae33786d-0547-49cc-ad39-235b496b2326" />

Renamed the Windows Server machine to DC01 to identify it as the first domain controller in the lab.
<img width="1004" height="781" alt="image" src="https://github.com/user-attachments/assets/9e31301e-6611-4e92-a1e9-f03c6b070e2f" />

Configured a static IP address on DC01 so the domain controller and DNS services remain reachable by client machines.
<img width="871" height="669" alt="image" src="https://github.com/user-attachments/assets/5b9ac52f-d22b-4a78-a4ca-8fd0b38ce0ef" />

Installed the Active Directory Domain Services role on DC01 to prepare the server for domain controller promotion.
<img width="983" height="672" alt="image" src="https://github.com/user-attachments/assets/697fd035-0287-4690-a40c-d6be076f7e7d" />

Promoted DC01 to a domain controller and created a new Active Directory forest named helpdesk.local.
<img width="905" height="616" alt="image" src="https://github.com/user-attachments/assets/71822379-d6b7-44fd-b7ba-5df370cdb977" />

Verified that Active Directory Users and Computers was available after promoting DC01 to a domain controller
<img width="1040" height="728" alt="image" src="https://github.com/user-attachments/assets/a96cc6b2-805f-4902-971d-27d65a6f79e4" />

Created Organizational Units in Active Directory to organize users, computers, groups, and departments. Also created test domain user accounts in Active Directory to simulate employee onboarding in a help desk environment.
<img width="752" height="531" alt="image" src="https://github.com/user-attachments/assets/09810f1e-7e39-4830-a20b-c52444d902d3" />
<img width="756" height="528" alt="image" src="https://github.com/user-attachments/assets/fc82a697-3f85-46a8-b996-522de5506b11" />

Created Active Directory security groups and assigned test users to simulate department-based access control.
<img width="750" height="525" alt="image" src="https://github.com/user-attachments/assets/7aa35b25-bbfe-48c4-a89e-080ea48efb8c" />

Created a shared folder 
<img width="756" height="588" alt="image" src="https://github.com/user-attachments/assets/1e3961df-cded-438c-a979-5a489b00a3f7" />

Edited the shared folder permissions
<img width="752" height="584" alt="image" src="https://github.com/user-attachments/assets/1034e1d4-9ff2-4864-86da-6c989484afd5" />

Gave HR,Sales,and IT folders different permissions.
<img width="749" height="671" alt="image" src="https://github.com/user-attachments/assets/3a94be2f-0fcb-4c2c-b8c6-fde6c534a8b1" />
<img width="730" height="562" alt="image" src="https://github.com/user-attachments/assets/f450b7da-db85-4fbe-9f4e-8f59ef6ad34a" />
<img width="713" height="555" alt="image" src="https://github.com/user-attachments/assets/72abea6b-5ddd-4045-8a67-7019ca932d81" />
Now that I completed some task on the Domain Controller. I've started creating the Windows Client to connect to it.
<img width="1172" height="806" alt="image" src="https://github.com/user-attachments/assets/f21872d1-b5b6-4917-abe3-f63b22e11b7f" />

Made sure NAT was enabled in Network Settings
<img width="784" height="509" alt="image" src="https://github.com/user-attachments/assets/23b62823-9d0a-4ba5-a69c-053a5ecaeb40" />

Installing windows 10 pro as it is need to join the domain
<img width="662" height="499" alt="image" src="https://github.com/user-attachments/assets/c4a4a64c-4285-456d-bf7f-d9f79724af54" />

Set up Windows Client renamed it Client01
Verified that DC01 was running with Active Directory Domain Services and DNS installed before joining the client computer to the domain.
<img width="1021" height="768" alt="image" src="https://github.com/user-attachments/assets/279ad5a9-4dda-4382-bb9a-58de282f7a5e" />
Confirmed DC01 static IP address before configuring the Windows client DNS settings.
<img width="1043" height="645" alt="image" src="https://github.com/user-attachments/assets/e4691024-9877-4ead-9a3c-21f7a0635cb1" />

Set up client01's static IP
<img width="398" height="452" alt="image" src="https://github.com/user-attachments/assets/cbfc4217-b157-4a0b-92ed-ae79b17aa2e7" />

Verified CLIENT01 could resolve the helpdesk.local domain to DC01 at 192.168.10.10.
<img width="445" height="172" alt="image" src="https://github.com/user-attachments/assets/aa986d08-cb5a-4a30-8bb8-02e8a5e89013" />

Successfully joined CLIENT01 to the helpdesk.local Active Directory domain.
<img width="978" height="723" alt="image" src="https://github.com/user-attachments/assets/5b7e29c5-0057-4fc3-9df8-bbd9b3d51d2f" />

Logged into CLIENT01 using the Active Directory domain user account HELPDESK\jsmith.
<img width="1029" height="764" alt="image" src="https://github.com/user-attachments/assets/90862d9c-abb1-49d2-9376-4ee8469e48b4" />

Verified that CLIENT01 was logged in as the Active Directory user HELPDESK\jsmith.
<img width="691" height="475" alt="image" src="https://github.com/user-attachments/assets/5cfba70d-9fd5-49c4-a57f-f7ef4bddbb4f" />

Accessed the shared company folder from CLIENT01 using the DC01 network path.
<img width="1015" height="710" alt="image" src="https://github.com/user-attachments/assets/33bc3e5b-0866-4ea8-90fa-2d453f64099a" />

Also made a mistake of giving everyone access to folders. Fixed permission for folders so that everyone in their respected roles have their permissions.
Restricted the IT shared folder so only IT-Staff, Administrators, and SYSTEM have access.
<img width="763" height="518" alt="image" src="https://github.com/user-attachments/assets/147ce5af-d52f-4bcf-9218-bf622dcafdba" />
<img width="762" height="515" alt="image" src="https://github.com/user-attachments/assets/ac425fe5-bf0d-4d1e-bbac-e444dbe9ab51" />
<img width="760" height="511" alt="image" src="https://github.com/user-attachments/assets/6c7ff66e-7e81-4a23-a7ef-a98ff2725192" />

Restricted the IT shared folder so only IT-Staff, Administrators, and SYSTEM have access.
<img width="770" height="581" alt="image" src="https://github.com/user-attachments/assets/1a609901-c445-4bba-b6c4-63043d52c7f9" />

Confirmed that John Smith doesn't have access to Sales folder
<img width="759" height="524" alt="image" src="https://github.com/user-attachments/assets/51cb7593-9726-41f5-a57b-7766059cb2ea" />

Added Jsmith to ITstaff to grant access to IT shared folder.
<img width="759" height="524" alt="image" src="https://github.com/user-attachments/assets/7c7562a4-1e07-427a-ba38-07167b158f15" />

Verified that jsmith could access the IT shared folder after being added to the IT-Staff group.
<img width="784" height="585" alt="image" src="https://github.com/user-attachments/assets/7b73c57e-19b2-4c44-ac2e-a7d9eaba229c" />

Verified that Jsmith still does not have access to sales and HR files
<img width="778" height="588" alt="image" src="https://github.com/user-attachments/assets/ad2c3956-6d0b-453a-90ef-fef875447d13" />

Reset the password for the domain user mgarcia and required the user to change it at next logon.
<img width="746" height="517" alt="image" src="https://github.com/user-attachments/assets/d4261a0c-3b23-4521-8d00-5be16847bd86" />

Verified that the user was required to change their password after a help desk password reset.
<img width="1012" height="764" alt="image" src="https://github.com/user-attachments/assets/487cb091-8dcc-464e-b077-d7a3707a657f" />

Confirmed successful login after resetting the Active Directory user password.
<img width="540" height="240" alt="image" src="https://github.com/user-attachments/assets/caec199c-b44a-4c72-bd9d-47ef02f75793" />

Simulated a user login issue by entering an incorrect password for the domain user Dlee. 
<img width="870" height="635" alt="image" src="https://github.com/user-attachments/assets/b773454b-c9e8-4d1c-8520-623cbd8a4917" />

Unlocked User DLee using Domain Controller.
<img width="746" height="512" alt="image" src="https://github.com/user-attachments/assets/696a672f-4c69-4e0a-a85a-1ef2c28cc027" />

Reset the password for dlee and required the user to change it at next logon.
<img width="747" height="524" alt="image" src="https://github.com/user-attachments/assets/e6cc6239-07a1-4d7d-bb7f-6c7f99496255" />

Confirmed that dlee could log in after the account was unlocked and the password was reset.
<img width="748" height="717" alt="image" src="https://github.com/user-attachments/assets/285a3925-0519-4bd7-ab6d-572c07a894a5" />

Created and linked a Group Policy Object to the HELPDESK-LAB organizational unit.
<img width="794" height="417" alt="image" src="https://github.com/user-attachments/assets/a77c1fac-38e9-4fd6-8367-bc0eee558b97" />

Configured a Group Policy login banner to display an authorized-use warning before domain sign-in.
<img width="781" height="551" alt="image" src="https://github.com/user-attachments/assets/94768028-4e2c-441c-a0ee-c79275582e99" />
<img width="775" height="555" alt="image" src="https://github.com/user-attachments/assets/7dc7d7b8-1526-45f8-82df-d35e959cece4" />

Moved CLIENT01 into the HELPDESK-LAB Computers OU so it can receive the linked Group Policy settings.
<img width="747" height="519" alt="image" src="https://github.com/user-attachments/assets/10ad4973-848d-408d-ac7e-8193b880598a" />

Updated group policy with command prompt and gpupdate /force
<img width="583" height="344" alt="image" src="https://github.com/user-attachments/assets/634d98d6-eb2c-4c23-86bb-5395a4d262bb" />

Verified that the Group Policy login banner appeared on CLIENT01 before user sign-in.
<img width="893" height="474" alt="image" src="https://github.com/user-attachments/assets/289ca441-50f5-441e-b62f-7394c19d719c" />

Thats all I've done for now. I will continue to work and see what I can do on this project!


