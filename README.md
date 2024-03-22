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
Displays the initial network scan identifying open ports and running services, setting the stage for deeper vulnerability assessment. Notably, services like Microsoft Terminal Services on port 3389, which may be vulnerable to unauthorized remote access if not properly secured.

![Screenshot (77)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/e53648e8-41bf-47bc-bb84-3ebbcee6e8cf)
Highlights missing HTTP security headers, indicating susceptibility to XSS and clickjacking, crucial for understanding web service security.


![Screenshot (79)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/84e21832-76d6-4337-b379-13f60b13e22c)
Shows detailed findings from a web server scan, revealing LDAP management interfaces and default page configurations that could lead to information disclosure or unauthorized modifications.


![Screenshot (80)](https://github.com/fypm2000/Network-Enumeration/assets/117059426/34eab6d5-b90a-4504-84b5-7a2e0c02831f)
Summarizes key vulnerabilities such as exposed administrative interfaces on SharePoint, outdated service versions, and server configurations that might be exploited by attackers.
