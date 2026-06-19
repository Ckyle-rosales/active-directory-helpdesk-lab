# active-directory-helpdesk-lab
# Active Directory Help Desk Lab
------------------------------------------
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
https://cdn.discordapp.com/attachments/1507498943251087481/1507500071732904007/image.png?ex=6a366199&is=6a351019&hm=655d8f5da797227d59f13c4ac8a575e517a2c28e593f048a758ce803d94c0f32&

Installed Windows Server Standard Evaluation with Desktop Experience for the Active Directory domain controller.
https://cdn.discordapp.com/attachments/1507498943251087481/1507501338915901611/image.png?ex=6a3662c7&is=6a351147&hm=fa9b356cf0aab44df63a23046f794727355a25f6c41bb7a91d5c0cfbfe85a45a&
Logged into Windows Server and opened Server Manager to begin configuring the domain controller.
https://cdn.discordapp.com/attachments/1507498943251087481/1507502647173841106/image.png?ex=6a3663ff&is=6a35127f&hm=a8b8a1062a7f2fdf7fe4be84ab2d435c0a68a2489873c0e0ee05290b2a54f877&
Renamed the Windows Server machine to DC01 to identify it as the first domain controller in the lab.
https://cdn.discordapp.com/attachments/1507498943251087481/1507503230257598494/Screenshot_2026-05-22_145439.png?ex=6a36648a&is=6a35130a&hm=37c72b345684d2da77c6000bbc6e6e03386c66b644a8d3749a60e520587102f2&
Configured a static IP address on DC01 so the domain controller and DNS services remain reachable by client machines.
https://cdn.discordapp.com/attachments/1507498943251087481/1507504015171260537/image.png?ex=6a366545&is=6a3513c5&hm=3aafefa42334702284dbc66817c75a7d049e5b0387dbec8dd5a63f6072406e7e&
Installed the Active Directory Domain Services role on DC01 to prepare the server for domain controller promotion.
https://cdn.discordapp.com/attachments/1507498943251087481/1507504495880437922/image.png?ex=6a3665b7&is=6a351437&hm=7006c878e0a1a03d5e969bf9183dfa178fd235abce5bab91cb6570fe20ed8534&
Promoted DC01 to a domain controller and created a new Active Directory forest named helpdesk.local.
https://cdn.discordapp.com/attachments/1507498943251087481/1507505838607306763/image.png?ex=6a3666f8&is=6a351578&hm=b27af9302332d8f2bbfe7b178607d0ba06b9f61e44eb68b8660308f3b0f0bca7&
Verified that Active Directory Users and Computers was available after promoting DC01 to a domain controller
https://cdn.discordapp.com/attachments/1507498943251087481/1507508908657217598/image.png?ex=6a3669d3&is=6a351853&hm=aeefb89812229ada0b15ebe00363b8affe25e667e9b98aeb3a01979ccbcb19be&
Created Organizational Units in Active Directory to organize users, computers, groups, and departments. Also created test domain user accounts in Active Directory to simulate employee onboarding in a help desk environment.
https://cdn.discordapp.com/attachments/1507498943251087481/1507509583072071790/image.png?ex=6a366a74&is=6a3518f4&hm=21fd13cb2795e314d13960677e4b9f486723f93c8a78dd77eaeab1fcb6777f5a&
https://cdn.discordapp.com/attachments/1507498943251087481/1507510581450768534/image.png?ex=6a366b62&is=6a3519e2&hm=03b618ae3524799188420b7f81e61aa032ece638446226d71a03ca16d38ca072&
Created Active Directory security groups and assigned test users to simulate department-based access control.
https://cdn.discordapp.com/attachments/1507498943251087481/1507511373272449144/image.png?ex=6a366c1f&is=6a351a9f&hm=68cd7ac4ac79751d3f1a1ab1a1271e851e21a48347e32cdc1f3dc22a077c1a89&
Created a shared folder 
https://cdn.discordapp.com/attachments/1507498943251087481/1508225459673104565/image.png?ex=6a36622b&is=6a3510ab&hm=75f715856b0f8a78a523b0b7f1866ff00579594699f7b5a4d65ddf84af3d9022&
Edited the shared folder permissions
https://cdn.discordapp.com/attachments/1507498943251087481/1508225796689363065/image.png?ex=6a36627b&is=6a3510fb&hm=3f352b1a59a8a595ca04f4f211363975f7418656fd73a8876a4037f27f11d5a0&
Gave HR,Sales,and IT folders different permissions.
https://cdn.discordapp.com/attachments/1507498943251087481/1508226433271726111/image.png?ex=6a366313&is=6a351193&hm=c804596de865a3e2c7d32888ae9c68578c7fa633b267988c4d6d624455e4fc76&
https://cdn.discordapp.com/attachments/1507498943251087481/1508226864026747062/image.png?ex=6a366379&is=6a3511f9&hm=b93b96fa48642ba8ef2ee74e8f179046b0c1b3680dd7d7b7536083e10a9da447&
https://cdn.discordapp.com/attachments/1507498943251087481/1508227097246568611/image.png?ex=6a3663b1&is=6a351231&hm=deae5dee0852c0dee9cf563897c3063e648867f97505a6e8dd93c56b875a2216&
Now that I completed some task on the Domain Controller. I've started creating the Windows Client to connect to it.
https://cdn.discordapp.com/attachments/1507498943251087481/1508228053736882396/image.png?ex=6a366495&is=6a351315&hm=915bc65851229e54a87652b8a74196d6d6593649dfbd763e77b15a14ac21cbf5&
Made sure NAT was enabled in Network Settings
https://cdn.discordapp.com/attachments/1507498943251087481/1508228720052142140/image.png?ex=6a366534&is=6a3513b4&hm=fd1b31ef0c904b2fb2d6cbedcb0841c47c7afbefa38e39599823a184d258a557&
Installing windows 10 pro as it is need to join the domain
https://cdn.discordapp.com/attachments/1507498943251087481/1508229516374311063/image.png?ex=6a3665f2&is=6a351472&hm=4e5637a768a47a2cf95b00b47b14d5760b765b6e54aaee083b15800c5e2cd9c0&
Set up Windows Client renamed it Client01
Verified that DC01 was running with Active Directory Domain Services and DNS installed before joining the client computer to the domain.
https://cdn.discordapp.com/attachments/1507498943251087481/1517400498120953926/image.png?ex=6a36cd96&is=6a357c16&hm=383935a81cbbd307f8d29bf1a24b4fa94dc045edf6ba6c1677062eeb3fdfa61a&
Set up client01's static IP
https://cdn.discordapp.com/attachments/1507498943251087481/1517401157801086976/image.png?ex=6a36ce33&is=6a357cb3&hm=633623e622a3659746a37b172321f22a7826681292c72c5248c35472a4c92518&
Verified CLIENT01 could resolve the helpdesk.local domain to DC01 at 192.168.10.10.
https://cdn.discordapp.com/attachments/1507498943251087481/1517409761380008066/image.png?ex=6a36d637&is=6a3584b7&hm=0755f0e011bdd086657d451bff1ae74d647b7e0166dde379c94b7bcebd9cc9cd&
Successfully joined CLIENT01 to the helpdesk.local Active Directory domain.
https://cdn.discordapp.com/attachments/1507498943251087481/1517410181900668928/image.png?ex=6a36d69b&is=6a35851b&hm=2c9d2e6141cacf2e0ea1ad25102b480b94b03b5dce20edca5f6b4a931bb113a7&
Logged into CLIENT01 using the Active Directory domain user account HELPDESK\jsmith.
https://cdn.discordapp.com/attachments/1507498943251087481/1517411283916423320/image.png?ex=6a36d7a2&is=6a358622&hm=6be222a51765c4b06b1274dc52bd8eb165a7368ed8302761f49e72ba421688d7&
Verified that CLIENT01 was logged in as the Active Directory user HELPDESK\jsmith.
https://cdn.discordapp.com/attachments/1507498943251087481/1517609726567907429/image.png?ex=6a36e7b2&is=6a359632&hm=f8878c74435d56404ea387332a92b5e9db01ab2bf5a9803278802ad2bed84bad&
Accessed the shared company folder from CLIENT01 using the DC01 network path.
https://cdn.discordapp.com/attachments/1507498943251087481/1517610076368539769/image.png?ex=6a36e806&is=6a359686&hm=60947af4cd9b8704964fb8dd1ec2ef2f73a870faab0f365adfe43daf2522b0d2&
also made a mistake of giving everyone access to folders
fixed permission for folders so that everyone in their respected roles have their permissions.
Restricted the IT shared folder so only IT-Staff, Administrators, and SYSTEM have access.
https://cdn.discordapp.com/attachments/1507498943251087481/1517618764382736544/content.png?ex=6a36f01d&is=6a359e9d&hm=67b7dafa5e3fde7b2ae7df8b6c4491af6deed02056f3377c198dacf2fd4f485d&
https://cdn.discordapp.com/attachments/1507498943251087481/1517618791284998274/content.png?ex=6a36f023&is=6a359ea3&hm=5dfaa4ff93839339d99d33dfb40ffe64447b7f315243868cb15baf67f4530dc1&
https://cdn.discordapp.com/attachments/1507498943251087481/1517618836084359339/content.png?ex=6a36f02e&is=6a359eae&hm=cc0cf2fe4e3fd7584513816889806e34971b3c7945941e38b937bf84ca087291&
Restricted the IT shared folder so only IT-Staff, Administrators, and SYSTEM have access.
https://cdn.discordapp.com/attachments/1507498943251087481/1517619106264781010/image.png?ex=6a36f06e&is=6a359eee&hm=1797e6ebb327155be54dc0917c50e795c1aff97d62b5ede6361a3aeae5164bbb&
Confirmed that John Smith doesn't have access to Sales folder
https://cdn.discordapp.com/attachments/1507498943251087481/1517619106264781010/image.png?ex=6a36f06e&is=6a359eee&hm=1797e6ebb327155be54dc0917c50e795c1aff97d62b5ede6361a3aeae5164bbb&
Added Jsmith do ITstaff to grant access to IT shared folder.
https://cdn.discordapp.com/attachments/1507498943251087481/1517619821523763240/image.png?ex=6a36f119&is=6a359f99&hm=eb67f6408f4d41119013aff3f753ea2e31f33fff84d87c74a48a5dd24a1374a4&
Verified that jsmith could access the IT shared folder after being added to the IT-Staff group.
https://cdn.discordapp.com/attachments/1507498943251087481/1517620215180038234/image.png?ex=6a36f177&is=6a359ff7&hm=763bc4763c8f4d32f1d100119f9258bb3076222db400a5ac1ce2963ab233f81e&
Verified that Jsmith still does not have access to sales and HR files
https://cdn.discordapp.com/attachments/1507498943251087481/1517620458403401748/image.png?ex=6a36f1b1&is=6a35a031&hm=683b927bf051daf1b663c24f137c92c48dc7452c9a37846beeeb3c8996eaefff&
Reset the password for the domain user mgarcia and required the user to change it at next logon.
https://cdn.discordapp.com/attachments/1507498943251087481/1517621177395318805/image.png?ex=6a36f25c&is=6a35a0dc&hm=9ae0a01b64d1a0838366cad2adf39eac6d7b77e033c3a7aac559f7c2240ac0c3&
Verified that the user was required to change their password after a help desk password reset.
https://cdn.discordapp.com/attachments/1507498943251087481/1517621608129364209/image.png?ex=6a36f2c3&is=6a35a143&hm=9dcfcb86f9e4262b5e1de4752e8d9fe782c3a2a7019db85f552d5cba515f6cbe&
Confirmed successful login after resetting the Active Directory user password.
https://cdn.discordapp.com/attachments/1507498943251087481/1517621964343087174/image.png?ex=6a36f318&is=6a35a198&hm=b03f00ef163db110365a5e7beb9e84111d015fa71f6df4486a4231b7d91d0ad9&
Simulated a user login issue by entering an incorrect password for the domain user dlee. 
https://cdn.discordapp.com/attachments/1507498943251087481/1517623334471208960/image.png?ex=6a36f45f&is=6a35a2df&hm=af4b99bdee3985b1c8f18cd52e5f37c8744a390d092cb76e0b2aeed697d85993&
Unlocked User DLee using Domain Controller.
https://cdn.discordapp.com/attachments/1507498943251087481/1517623682036666488/image.png?ex=6a36f4b1&is=6a35a331&hm=39a5250c9bd5cadec4e4835cc3b98e17d8f34e8d38d39b79703f83182d1112e6&
Reset the password for dlee and required the user to change it at next logon.
https://cdn.discordapp.com/attachments/1507498943251087481/1517624342035300524/image.png?ex=6a36f54f&is=6a35a3cf&hm=c97918cfef3de8412208c11423694fbbaf4c7781bb6927949ae59e7387a97001&
Created and linked a Group Policy Object to the HELPDESK-LAB organizational unit.
https://cdn.discordapp.com/attachments/1507498943251087481/1517625227805462598/image.png?ex=6a36f622&is=6a35a4a2&hm=2529823ccc5166397e35b843725d53c0f5d717f0ef313f732d20895d6ed5091f&
Configured a Group Policy login banner to display an authorized-use warning before domain sign-in.
https://cdn.discordapp.com/attachments/1507498943251087481/1517626250410070118/image.png?ex=6a36f716&is=6a35a596&hm=0f3e865b97ef18b2985527ec91a5d1f1955e8576bfc7ccdc5f88f6fc487f24b9&
https://cdn.discordapp.com/attachments/1507498943251087481/1517626250682830858/image.png?ex=6a36f716&is=6a35a596&hm=77487f3d59da6a556c5b6f135844a0ecabd896fb61cf0af851a126a4ae262ef2&
Moved CLIENT01 into the HELPDESK-LAB Computers OU so it can receive the linked Group Policy settings.
https://cdn.discordapp.com/attachments/1507498943251087481/1517627092068733018/image.png?ex=6a36f7de&is=6a35a65e&hm=30661b332c349ae1cb267d716293d28d5ef7fe266878a10f4965e12c9354c116&
Updated group policy
https://cdn.discordapp.com/attachments/1507498943251087481/1517629071637483632/image.png?ex=6a36f9b6&is=6a35a836&hm=e8cb8e57755ff935bfd9778fc48c6b031925d7d695eb2c9a1ef242b4ef530c01&
Verified that the Group Policy login banner appeared on CLIENT01 before user sign-in.
https://cdn.discordapp.com/attachments/1507498943251087481/1517629344057659512/image.png?ex=6a36f9f7&is=6a35a877&hm=25f1c034a115e97b6e4ca3510fc95418e6c1a037b86861821d9610402020c22e&

