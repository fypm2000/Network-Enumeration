# Network-Enumeration

## Objective

The objective of this project was to perform a comprehensive network security assessment within a VM Lab environment. The main goal was to identify and analyze potential vulnerabilities and security weaknesses across the network infrastructure without compromising the integrity or stability of any systems. This assessment aimed to enhance knowledge and proficiency in network security principles and methodologies through practical application and analysis of scan results.

### Skills Learned

- Utilization of network scanning tools.
- Analysis of open ports and services to identify potential vulnerabilities.
- Understanding of security headers and their importance in web server security.
- Interpretation of scan results to assess network security posture.
- Enhanced knowledge of network protocols and security vulnerabilities.

### Tools Used

- Nmap, a versatile network scanning tool for discovering hosts, open ports, and services on a network
- Sparta, a Python-based GUI application for simplifying network penetration testing, offering streamlined access to various tools and scan results organization.

## Steps
Sparta Scan Results

![Screenshot (52)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/97e1be17-b87a-4ed8-a981-d564345906e3)
- Displays the initial network scan identifying open ports and running services, setting the stage for deeper vulnerability assessment. Notably, services like Microsoft Terminal Services on port 3389, which may be vulnerable to unauthorized remote access if not properly secured.

192.168.101.197 (Port 80/tcp)
![Screenshot (76)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/0783dcb7-bd16-40c2-a831-4299e69e0dab)
- Missing X-Frame-Options header: Without this header, the website could be vulnerable to clickjacking attacks, where an attacker could trick a user into clicking on something different than what the user perceives, potentially revealing confidential information or taking control of their account.
  
- Missing X-XSS-Protection header: This header enables the cross-site scripting (XSS) filter built into most browsers. Not having it means that the website is more susceptible to XSS attacks, where attackers could inject client-side scripts into web pages viewed by other users, potentially leading to data theft or malicious redirection.

- Missing X-Content-Type-Options header: This prevents the browser from interpreting files as a different MIME type than what is specified by the content-type in the HTTP headers. Without this, attackers could perform MIME-type sniffing attacks, leading to security loopholes where content is executed with incorrect MIME types, such as executing non-executable files.


192.168.101.151 (Port 1947/tcp)
![Screenshot (77)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/e53648e8-41bf-47bc-bb84-3ebbcee6e8cf)

- HASP LM 11.5.00: This is likely a license management server used for software protection. If vulnerabilities exist in this service, they could be exploited to bypass software licensing checks or disrupt license management on the network, affecting business operations and potentially enabling software piracy.
  
- The same missing security headers as above, missing HTTP security headers, indicating susceptibility to XSS and clickjacking, crucial for understanding web service security. Indication a systemic issue with security configurations across the network.


192.168.101.153 (Port 1947/tcp)
![Screenshot (78)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/30259ef2-0b3d-4c9c-8f5d-55e5eb042f18)
- Potential web application vulnerabilities: XSS vulnerability in iLoMai.aspx, allows the potential for cross-site scripting attacks, threatening user data and browser security.

![Screenshot (79)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/84e21832-76d6-4337-b379-13f60b13e22c)
- Exposed LDAP service: Shows detailed findings from a web server scan, revealing LDAP management interfaces and default page configurations that could lead to information disclosure or unauthorized modifications.

![Screenshot (80)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/34eab6d5-b90a-4504-84b5-7a2e0c02831f)
- Summarizes key vulnerabilities such as exposed administrative interfaces on SharePoint, outdated service versions, and server configurations that might be exploited by attackers.

192.168.101.153 (Port 5357/tcp)
![Screenshot (81)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/ef97d5c7-20ed-4ad2-b0cb-4da206db73b3)

- Microsoft HTTPAPI/2.0: Indicates a web service that, if not properly secured, could be targeted by attackers.
  
- Lack of security headers, similar to other IP addresses, it poses risks such as clickjacking and XSS attacks.


192.168.101.157 (Port 1947/tcp)
![Screenshot (82)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/576f6c51-40cb-4ed4-85cc-66cc8fa727c6)

- HASP LM/15.00: Indicates an updated version of the license management service that, if exploitable, could lead to similar risks as mentioned for 192.168.101.151.
