<h4>Tenant Level Logging</h4>
<p>I will be collecting and managing logs for all resources and services.

<p>
<img src="https://github.com/user-attachments/assets/ee0a06de-b17a-43ec-8ebb-06b5012e5fec" height="80%" width="80%" />
</p>
<p>I created a diagnostic setting name called audit-signin, which is able to check auditlogs and signinlogs, which will be sent to the CyberLab workspace.</p>
<p>
<img src="https://github.com/user-attachments/assets/e9430fe6-d60c-431b-a87d-2352595b70b1" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/f42c7455-16a7-4638-a1b5-cda7529c33b6" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/b0f8717c-8f17-4f53-ac13-5f0da788f468" height="80%" width="80%" />
</p>
<p>I created a new user in Active Directory called Sandrajackson and was able to log into her account in a private browser. 
  I was able to assign Sandrajackson as a Global Admin role.
<br />
<p>
  <img src="" height="80%" width="80%" />
</p>
<p>
Detecting a brute-force attack attempt by failed login events (EventID '4625') in the last 60mins. As you can see, I grouped the failures by source IP address and counts the number 
  of the failed attempt. If any IP address has more than 10 failed login attempts within 60mins, it's now flagged as a brute-force attack.
  <p>
<img src="" height="80%" width="80%" />
    <img src="" height="80%" width="80%" />
</p>
<p>
There are other ways you can troubleshoot this and getting the same results. Using EventID '4625' to filter the SecurityEvent logs for failed login attempts in the last 60mins. 
  Using LogonType3 to focus on network logons like RDP and SMB. Summarizing the IP Address and counting the number of failed attempts by each IP Address and destination host.
  Any IP Address with over 5 login attempts is a potential brute-force attack.
</p>
<br />
 <p>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</p>
<p>
I wanted to detect Malware on Microsoft Window's EventLog either on the ID '1151' or '1150', which detects scanning or malware events on the Windows Defender actions. Since the
  Eventlevel is a 4, it's nothing too concerning, it means information. Which provides informational msgs about system or application operations.
</p>
<br />
