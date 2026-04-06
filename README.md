# Making-The-Domain-Controller 

<h2>Overview</h2>
Here is my documentation how I set up the domain controller for my domain controller.
<br /> 

<h2>Setting Up The Domain Controller</h2>

For the Domain Controller’s image, I am picking windows server 2022.

<img width="761" height="59" alt="Snapshot#9" src="https://github.com/user-attachments/assets/1c990b35-7075-40ee-a7e3-35c7d3da22b4" />



Under the networking section, I will select the Vnet I made for the dealership and I will place it on the Server-Subnet. 

<img width="823" height="104" alt="Snapshot#10" src="https://github.com/user-attachments/assets/7249c586-4e05-4198-80c2-9205f7f5adf8" />



The Domain controller VM is now created. 

<img width="580" height="110" alt="Snapshot#11" src="https://github.com/user-attachments/assets/d17bb68c-1250-4be4-8692-f754ef81102d" />



I will log in to the Domain Controller VM remotely with RDP. 

<img width="412" height="254" alt="Snapshot#12" src="https://github.com/user-attachments/assets/05550361-976c-472f-94c5-30fce4664a11" />



Once I am logged in, I will install active directory on this VM. I will go to the server manager and click “Add Roles and Features”. 

<img width="1454" height="778" alt="Snapshot#13" src="https://github.com/user-attachments/assets/7d5996f9-0242-4b0e-92d2-39715694c525" />



I will go to server roles and select “Active Directory Domain Services”. I’ll just click next on everything and let Active Directory Install. 

<img width="807" height="578" alt="Snapshot#14" src="https://github.com/user-attachments/assets/7969d368-19c3-476e-971f-fc7b7f153cee" />



Active Directory is now installed on the VM. 

<img width="821" height="583" alt="Snapshot#15" src="https://github.com/user-attachments/assets/7f70cd41-b414-48df-97e0-b83bd32a232a" />



With Active Directory now installed, I now have to promote the VM to a real Domain controller. I will click on the flag on the top right side and click “promtoe this server to a domain controller”. 

<img width="587" height="391" alt="Snapshot#16" src="https://github.com/user-attachments/assets/baddc32a-2db1-40bb-bbe0-faacb9e7cd30" /> 



I will select “Add a new forest” and I type the root domain name “dealership.com”. I will leave evey toher setting as default and click install. This will restart the VM.   

<img width="787" height="582" alt="Snapshot#17" src="https://github.com/user-attachments/assets/4fbc3ac6-7632-40c1-bf18-76d749716279" />  



When I log back in to the Domain Controller, I have to specify the domain I want to log in to and the account within that domain. Our domain name is dealership.com, so I will log in like this, "dealership.com\labuser". It is important to use "\" instead of "/".

<img width="475" height="385" alt="Snapshot#18" src="https://github.com/user-attachments/assets/191fcc8b-0f37-4398-9e06-d11c986e729a" /> 



Logging back into the Domain controller, I can now access administrative tools like “Active Direcotry Users and Computers”. This is something I will be using a lot to manage user accounts and computers in the domain.

<img width="906" height="575" alt="Snapshot#19" src="https://github.com/user-attachments/assets/4a0c8f11-7142-432e-b2d8-0390fd722319" />



 



