PENETRATION TESTING REPORT
FOOTPRINTING & NETWORK SCANNING PHASES
W2-PM-FINAL | CYBERSECURITY |  NETWORKWALKS

Pentester Name
(Cybersecurity Intern)	Naima Sultana
Program/Batch	B084-Networkwalks
Date	12 November 2026
Modules completed	
W2-PM1 – Multiple Kali Tools
W2-PM2 – Google Hacking Database (GHDB)
W2-PM3 – theHarvester
W2-PM5 – Zenmap Scanning


Client/Target	1. Networkwalks (secured written permission already)
2. My own local LAN Network
Permission secured from client?	Yes
Phases covered	Phase 1: Reconnaissance & Footprinting
Phase 2: Scanning & Network Discovery
Phase 3-5: In Progress

1. Liability Disclaimer
I have performed these activities only on the systems & devices where I had secured written permission or the devices/systems that I own myself. All these materials are for education and research purpose only. Do not use anything from here to break the law. The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility. Misuse can lead to criminal charges, heavy fines, loss of your job and a permanent record. In most countries unauthorised access is a crime even when nothing is damaged.
2. Introduction
This report documents the practical activities completed during Week 2 of my Cybersecurity Internship Program at NetworkWalks.
The report focuses on two major phases of penetration testing: Footprinting & Reconnaissance and Scanning & Network Discovery.
Four practical modules were completed using different cybersecurity tools and techniquesThe first module involved collecting publicly available information about the NetworkWalks domain using Kali Linux tools such as WHOIS, WhatWeb, Nslookup, cURL, Wafw00f, and DNSRecon.
The second module focused on Google Hacking Database (GHDB), where Google search operators were used to identify publicly indexed mathematics PDF resources and investigate camera-related search exposure.
The third module involved using theHarvester in Kali Linux to collect publicly available email addresses and subdomains associated with Microsoft.com through Baidu and multiple information sources.
The fourth module involved using Zenmap (Nmap GUI) to discover active devices on my own local network, identify their IP and MAC addresses, and generate a network topology.
Each activity helped me understand how cybersecurity professionals collect information, identify network assets, analyze publicly available data, and document potential security risks before conducting further security assessments.
3. Tools Used
Tool	Purpose
Kali Linux	Operating system for cybersecurity and reconnaissance activities
WHOIS	Collect domain registration information
WhatWeb	Identify website technologies and web application components
Nslookup	Resolve domain names into IP addresses
cURL	Inspect HTTP response headers
Wafw00f	Identify Web Application Firewalls
DNSRecon	Enumerate DNS records
Google Search	Search publicly indexed information
GHDB	Discover information using Google dorks
theHarvester	Gather publicly available email addresses and subdomains
Baidu	Search source used by theHarvester
Zenmap	Perform network discovery and visualize network topology
Nmap	Discover live hosts on a network
Windows CMD	Identify local IP configuration
4. Activities Performed
4.1 Module 1 – Footprinting & Reconnaissance Using Multiple Kali Tools (W2-PM1)
I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f and DNSRecon. Each tool was used to collect a different type of information about the target.
First, I used WHOIS to obtain publicly available domain registration information and identify the domain’s name servers. The results provided information about the domain registration and hosting infrastructure.
I then used WhatWeb to identify technologies used by the website. The results identified WordPress 7.1.4 and WP Download Manager 3.3.76, along with other information exposed by the website.
Using Nslookup, I resolved the domain name to its IP address. The provided result identified 192.232.216.135.
I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and exposed the WordPress REST API endpoint /wp-json/.
Next, I used Wafw00f to determine whether a Web Application Firewall was protecting the website. The result identified ModSecurity (SpiderLabs).
Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records and DNS software information.

4.2 Module 2 – Google Hacking Database (GHDB) (W2-PM2)
Objective
To understand Google Hacking Database and use Google dorks to identify publicly indexed information, including mathematics PDF resources and camera-related web exposure.
Background
Google Hacking Database (GHDB) is a collection of Google search queries known as Google dorks. These queries use search operators to identify publicly indexed information that may reveal sensitive or unintentionally exposed resources.
GHDB is hosted by Exploit Database and is used by security researchers and penetration testers during passive reconnaissance.
Website: https://www.exploit-db.com/google-hacking-database
Task 1: Identify Camera-Related Search Results
Objective: To investigate camera-related search results using GHDB and Google search operators.
Methodology:
1.	Opened the Exploit Database website.
2.	Navigated to Google Hacking Database.
3.	Searched for camera-related entries using keywords such as camera and webcam.
4.	Selected relevant Google dorks.
5.	Copied the dorks and searched them using Google.
6.	Examined the search results and classified the exposed resources.
7.	Recorded authorized and verifiable findings.
Findings Table:
No.	Link / Finding	Relevant Dork	Username/Password
1	http://109.233.191.130:8080/	intitle:"webcamXP" inurl:8080

2	http://153.156.0.199/CAM/2023/03/	intitle:"Index of /cam/"
 	
3	http://202.153.140.18:8106/	intitle:"IP CAMERA" "User Login" "User Name" "Password" "Preview Stream"

4	http://99.114.240.169:8080/	intitle:"Webcam" inurl:WebCam.htm	
5	http://80.152.138.183/ViewerFrame?Mode=Motion&Language=0	allintitle: "Network Camera NetworkCamera"	
6	http://95.255.183.164:8080/multi.html	intitle:webcam 7 inurl:8080 -intext:8080

7	http://219.111.32.218:8088/viewer/live/index.html	inurl:viewer/live/index.html

8	http://139.64.168.120:8080/	intitle:"webcamxp 5" intext: "live stream"	
9	http://75.149.26.30:1024/	intitle:"webcamxp 5" intext: "live stream"	
10	http://184.57.102.6:5432/	intitle:"webcamxp 5" intext: "live stream"	
Task 2: Find Mathematics eBooks in PDF Format
Objective: To identify publicly accessible listings containing downloadable mathematics eBooks in PDF format using Google dorks.
Methodology:
1.	Opened Google Search.
2.	Entered mathematics-related Google dorks.
3.	Examined search results for directory listings.
4.	Opened relevant publicly available listings.
5.	Identified mathematics-related PDF documents.
6.	Verified that the resources were available for legitimate public download.
7.	Recorded the listing URLs and corresponding dorks.



Findings Table:
No.	Link	Relevant Dork	Username
/Password
1	https://education.giakonda.org.uk/Maths/?SD	intitle:index.of "parent directory" mathematics pdf	N/A
2	https://justmathbg.info/files/	intitle:index.of "parent directory" mathematics pdf	N/A
3	https://netlib.org/math/docpdf/	intitle:index.of "parent directory" mathematics pdf	N/A
4	 https://theswissbay.ch/pdf/Books/Mathematics/	intitle:"index of" mathematics books pdf	N/A
5	http://erewhon.superkuh.com/library/Math/	intitle:"index of" mathematics books pdf	N/A
6	https://www.aetkin.com/files/Math%20150%20Calculus%20I/
Advanced%20Calculus%20Textbook/	intitle:"index of" calculus pdf	N/A
7	https://isidore.co/CalibreLibrary/Euler,%20Leonard/
Foundations%20of%20Differential%20Calculus%20(4899)/	intitle:"index of" calculus pdf
	N/A
8	https://www.stat.cmu.edu/~brian/valerie/617-2022/week07/spline%20references/
John%20H%20Mathews%20Numerical%20Methods/	intitle:"index of" "numerical methods" pdf	N/A
9	https://onlinelibrary.wiley.com/doi/10.1002/9781118557877.index1	intitle:"index of" "numerical methods" pdf	N/A
10	https://www.e-booksdirectory.com/mathematics.php	intitle:index.of "parent
directory" mathematics pdf	N/A



4.3 Module 3 – Email and Subdomain Enumeration Using theHarvester (W2-PM3)
Objective
To collect publicly available email addresses and subdomains associated with the target organization Microsoft.com using theHarvester in Kali Linux.
Background
theHarvester is an open-source reconnaissance tool used to gather publicly available information about an organization.
It can collect information such as:
•	Email addresses.
•	Subdomains.
•	Hostnames.
•	IP addresses.
•	Publicly indexed infrastructure information.
The tool uses different public information sources, including search engines and other supported data sources.
Target
microsoft.com
Task 1: Email and Subdomain Enumeration Using Baidu
theHarvester is a Python tool, pre-installed in Kali Linux, that gathers emails, subdomains, hosts and employee names from public sources such as search engines. In the commands, -d is the target domain, -l limits the number of results and -b selects the data source. Output was saved to text files.
Task	Command	Source	Limit
Task 1	theHarvester -d microsoft.com -l 1000 -b baidu	Baidu	1000
Result	Task 1 (Baidu)
Emails found	1
Subdomains / hosts found	20
Task 2: Email and Subdomain Enumeration (from all sources)
Task	Command	Source	Limit
Task 1	theHarvester -d microsoft.com -l 50 -b all	All Source	50
Result	Task 1 (Baidu)
Emails found	3
Subdomains / hosts found	9962

4.4 Module 4 – Network Scanning Using Zenmap (W2-PM5)
The practical required me to identify my local IP and subnet, discover live hosts with their IP and MAC addresses, and generate a network topology.
Step 1: Local network information. I ran ipconfig in Windows Command Prompt. The active Wi-Fi adapter showed:
Item	Value
IPv4 address	192.168.0.106
Subnet mask	255.255.255.0
Default gateway	192.168.0.1
The adapter list also showed an Ethernet adapter at 192.168.56.1, which is not the network that was scanned.
Step 2: Ping scan. In Zenmap I entered the target 192.168.0.0/24 with the profile Ping scan. The command was nmap -sn 192.168.0.0/24. Nmap 7.993 scanned 256 IP addresses on 10 November 2026 at 22:07 (+06:00). Four hosts were up, and the scan finished in 8.82 seconds.
Host	Latency	MAC address	Vendor
192.168.0.1	0.029 s	D8:32:14:21:1E:B0	Tenda Technology Ltd. (the router/gateway)
192.168.0.100	0.12 s	9A:8B:85:24:0D:A2	Unknown
192.168.0.103	0.098 s	22:5E:D9:88:CE:7C	Unknown
192.168.0.106	n/a	not shown	My own PC (scan source)
The MAC addresses of .100 and .103 have an unrecognised vendor and the locally administered bit set. This commonly indicates randomised private Wi-Fi addresses, as used by modern phones, though I have not confirmed which devices these are. (Add the device names if you identify them.)
Step 3: Topology. I opened the Topology tab, enabled the legend and saved the graphic as a PDF. The map shows the gateway 192.168.0.1 at the centre with 192.168.0.100, .103 and .106 connected to it. All hosts appear green because this was a ping scan and no ports were scanned.
5. Risk Analysis and Impact
Based on the observations collected from the four practical modules, the following potential security risks were identified.
No.	Risk / Finding	Evidence / Observation	Potential Impact	Risk Level
1	Web technology information exposed	WhatWeb identified WordPress and WP Download Manager	May help attackers identify software requiring further security review	Medium
2	Server IP address identifiable	Nslookup resolved the domain to an IP address	Provides information about hosting infrastructure	Low
3	HTTP technical information exposed	cURL returned HTTP headers and REST API information	May assist technology fingerprinting	Low
4	WAF technology identifiable	Wafw00f identified ModSecurity	Reveals information about security architecture	Low
5	DNS infrastructure information exposed	DNSRecon identified DNS and mail records	May assist infrastructure reconnaissance	Medium
6	Publicly indexed directory listings	GHDB searches identified directory-related results	May expose unintended files if access controls are inadequate	Medium
7	Public mathematics PDF resources	Google searches identified downloadable PDF listings	Requires review of information disclosure and content distribution permissions	Informational
8	Email addresses and subdomains discoverable	theHarvester collected publicly indexed information	May assist phishing preparation and infrastructure mapping	Medium
9	Multiple live hosts discovered	Zenmap identified four active hosts	Unknown devices may require network inventory verification	Medium
10	Network device information exposed	Zenmap identified available MAC addresses and one manufacturer	May help build an internal network profile	Low
Risk Level Key:
•	Critical: Severe confirmed security impact.
•	High: Significant security concern.
•	Medium: Requires further investigation.
•	Low: Limited potential impact.
•	Informational: Observation without a demonstrated security risk.
The risks listed above are preliminary observations, not confirmed vulnerabilities. No exploitation or unauthorized access was performed as part of these activities.
6. Recommendations
Based on the activities performed, the following security recommendations are proposed.
6.1 Website Security
•	Regularly review publicly exposed website technologies.
•	Keep CMS platforms and plugins updated.
•	Remove unnecessary technical information from HTTP responses.
•	Review publicly accessible API endpoints.
•	Maintain appropriate WAF configurations.
6.2 DNS Security
•	Review DNS records periodically.
•	Remove outdated or unnecessary DNS records.
•	Protect sensitive DNS management information.
•	Monitor DNS changes and unexpected subdomain exposure.
6.3 Information Exposure
•	Review publicly indexed directory listings.
•	Disable unnecessary directory indexing.
•	Restrict access to sensitive files and resources.
•	Avoid exposing private camera interfaces or recordings.
•	Use appropriate authentication and access controls.
6.4 Email and Subdomain Security
•	Monitor publicly exposed organizational email addresses.
•	Implement SPF, DKIM, and DMARC.
•	Review discovered subdomains and remove unused services.
•	Monitor suspicious domains and phishing attempts.
•	Maintain an updated inventory of organizational assets.
6.5 Network Security
•	Perform regular internal network discovery.
•	Maintain an updated network asset inventory.
•	Investigate unknown or unexpected devices.
•	Segment networks where appropriate.
•	Restrict unauthorized access to network devices.
•	Monitor network activity and maintain appropriate access controls.
7. Learning Outcomes
After completing the four practical modules, I gained practical knowledge in the following areas:
1.	Understanding the footprinting and reconnaissance phase of penetration testing.
2.	Collecting publicly available domain registration and DNS information.
3.	Identifying web technologies and server information using Kali Linux tools.
4.	Understanding Google Hacking Database and Google search operators.
5.	Identifying publicly indexed resources using Google dorks.
6.	Understanding email and subdomain enumeration using theHarvester.
7.	Using different public information sources during reconnaissance.
8.	Understanding network discovery using Nmap and Zenmap.
9.	Identifying active hosts, IP addresses, and MAC addresses.
10.	Understanding network topology visualization.
11.	Documenting technical findings and assessing potential security impacts.
12.	Understanding the importance of authorization and ethical cybersecurity practices.
8. Conclusion
During Week 2 of my Cybersecurity Internship Program at NetworkWalks, I completed practical activities related to footprinting, reconnaissance, information gathering, and network scanning.
In Module 1, I used six Kali Linux tools to collect publicly available information about the NetworkWalks domain. These tools helped me understand domain registration, DNS resolution, web technology identification, HTTP headers, WAF detection, and DNS enumeration.
In Module 2, I explored the Google Hacking Database and learned how Google dorks can identify publicly indexed information and directory listings. I also practiced searching for mathematics-related PDF resources and understanding camera-related exposure.
In Module 3, I used theHarvester to gather publicly available email addresses and subdomains associated with Microsoft.com through Baidu and multiple supported sources. This helped me understand how automated reconnaissance tools collect information from public sources.
In Module 4, I used Zenmap to perform a Ping Scan on my own local network. The scan successfully identified four active hosts within the 192.168.0.0/24 subnet. I also learned how to examine IP and MAC addresses and visualize network topology.
Overall, these practical activities helped me understand how information gathering and network discovery contribute to the early stages of penetration testing. I also learned the importance of documenting findings, evaluating potential security risks, and performing all cybersecurity activities within an authorized scope.
9. Evidence and Screenshots
The following screenshots and supporting files will be included as evidence of the completed practical activities.
Module 1 – Multiple Kali Tools 
       











Module 2 – Google Hacking Database
    


Module 3 – theHarvester  
 

  




Module 4 – Zenmap
  
  
Author
Naima Sultana
Cybersecurity Intern
Program Information:
Program Name: Cybersecurity Internship Program
Week: 02
Modules: W2-PM1, W2-PM2, W2-PM3, W2-PM5
Organization: NetworkWalks

