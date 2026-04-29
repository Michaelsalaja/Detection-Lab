# Detection-Lab

## Objective

The Detection Lab project was geared towards showcasing my Security Operations skills by detecting IoCs and reviewing threat intelligence sources in my home Lab. Analyzing the IoCs with the exploration of publicly available threat intelligence sources will enable me as a Security Analyst to rapidly evaluate potential threats, understand their context, hunt for potential compromise, and initiate effective response measures.

### Skills Learned

I have learned the following:

 -	Detected and reviewed IoC as file hash, ip address, and domain name.
 -	Reviewed a file hash using VirusTotal, to determine file type, size, detection results, and associated malware family. The use of MalShare was unsuccessful due to an indefinite suspension of the platform after losing their host provider.
 -	Assessed an IP address through AbuseIPDB to evaluate its reputation, number of abuse reports, categories of abuse, and origin.
 -  Investigated a domain using Cisco Talos Intelligence to examine reputation score, web category, related IPs, historical data, and security alerts.

### Tools Used

To demonstrate the steps taken for the experiment in my home lab, I utilized the following free tools.
 -	VirusTotal: It is a powerful malware scanning service, created by a Spanish security company, which helps Security Analysts analyze suspicious files and URLs to uncover different types of malware behavious and malicious content through files, file hashes, and URL. There is disadvantage when 	sensitive data are uploaded on VirusTotal, given the fact that anyone who pays for VirusTotal usage gets an access to any uploaded file and can download that file. This is why VirusTotal emphasized clearly that it is not responsible for any data uploaded on its platform.
 -	MalShare: It is platform of a free malware repository, that provides researchers access to samples and malicious feeds used to analyze file hashes as IoCs, identify malicious files and gather threat intelligence about malware.
- 	AbuseIPDB: It is a platform that is used to review IP addresses as IoCs, which helps provide information on malicious activity, abuse reports and reputation for threat analysis.

- 	Cisco Talos Intelligence: This platform is used is used to investigate domains or URLs as Iocs, evaluating its reputation, related Ips, and security alerts to support threat intelligence.

## Steps

PART A: Reviewing a File Hash with MalShare / VirusTotal

During this project, MalShare website was shut down after losing their host provider, which made me switch to VirusTotal.

Step 1

 -	I double-clicked Google Chrome   in my desktop for opening and typed in: https://virustotal.com/ in the address bar.

 -	In the Quick Search bar, I typed in a hash value of 44d88612fea8a8f36de82e1278abb02f, which I obtained for analysis and pressed Enter.

EICAR

 -	This hash value is extracted from virus, named EICAR. It is test string used for detecting and testing antivirus software. It is “dummy virus” that provokes an Antivirus engine trigger an alert.

- 	This helps Antivirus engines to demonstrate their ability to recognize signature-based malwares and neutralize their threats.

<img width="511" height="85" alt="image" src="https://github.com/user-attachments/assets/0e050ed0-9155-41d9-ad2a-089948a173f6" />
                                                            Figure 1: Code Insights

Step 2

Given the output below in the details section, 66 out of 68 security vendors flagged EICAR as malicious although, it is a virus test file.

   <img width="468" height="288" alt="image" src="https://github.com/user-attachments/assets/beb2c35f-e68a-4086-ac13-a9d022f6f2ef" />
                                                            Figure 2: EICAR Virus
                                                             
<img width="527" height="265" alt="image" src="https://github.com/user-attachments/assets/b8dbfe32-3d58-436b-9be2-f13229e7cc32" />
                                                            Figure 3: EICAR Virus     
                                                                                                                                      
  <img width="527" height="265" alt="image" src="https://github.com/user-attachments/assets/337bc247-3174-41fd-bb04-9f50499563f7" />                                                                                      Figure 4: EICAR Virus           

 -	I analyzed the test string to know their verdict, reputation scores, what various antivirus engines who are designed to recognize EICAR perceive the EICAR virus to be, including the comments from community to provide me with additional contacts for my investigation.
                                                           
<img width="515" height="338" alt="image" src="https://github.com/user-attachments/assets/1f581a71-a685-4764-ba9e-08986bded3f0" />
                                                         Figure 5: Details Section
                                                          
- 	In the details section, the history, properties, and the signature names of the EICAR virus are contextualized. This text string was first detected by the offensive security vendors on June 14, 2012. The MD5 hash, SHA-1, SHA-256 sum are depicted as properties of the powershell file. In exceptions of SHA-256, MD5 and SHA-1 are weak algorithm s that can allow collision. Weak algorithms like MD5 and SHA-1 constitute cryptographic vulnerabilities, allowing collision attacks, reducing password security. Notable real-world examples are 
	Heartbleed (OpenSSL) – exposed encrypted communications
	KRACK (WPA2) – allowed Wi-Fi traffic interception

<img width="548" height="281" alt="image" src="https://github.com/user-attachments/assets/7bff69e3-1a74-4af1-9be2-492373d3e995" />
                                                           Figure 6.1: Relations Sections           
                                       
<img width="468" height="295" alt="image" src="https://github.com/user-attachments/assets/1be7ed73-65f4-4881-9c61-0535e64e51a6" />
                                                           Figure 6.2: Relations Sections

- 	The Relations Section shows us various kinds of Domains that were contacted by the EICAR virus, the IP addresses that came in contact with the “Dummy Virus,” including Execution parents, and Dropped Files These provide us additional context for investigating this file hash file.
                                               
  	<img width="564" height="337" alt="image" src="https://github.com/user-attachments/assets/ec5475a0-7d81-49aa-9f9b-a8586f61c53a" />
                                                         Figure 7: Behavior Section

  	<img width="521" height="473" alt="image" src="https://github.com/user-attachments/assets/84cf439c-74c4-4361-9941-071ad472a2a9" />
                                                          Figure 8: MITRE ATT&CK

The Behavior Section provides us with MITRE Attack tactics and techniques in form of signatures, Intrusion Detections Systems (IDS) Rules, SIGMA Rules, Dropped Files, Network communications.

<img width="509" height="262" alt="image" src="https://github.com/user-attachments/assets/d33bdb3e-6591-4b54-9593-9dd2549666d4" />
                                                          Figure 9: Community Section


- This Community Section gives us an overview of vendors or threat hunters behind the creation of the EICAR signature file.

PART B: Reviewing an IP Address with AbuseIPDB

Step 1

 In the address bar, I typed in https://www.abuseipdb.com/ and verified the captcha
 
<img width="468" height="241" alt="image" src="https://github.com/user-attachments/assets/f0402212-426d-4183-b97a-6e69f16769d6" />
                                                          Figure 10.1: Homepage

<img width="506" height="261" alt="image" src="https://github.com/user-attachments/assets/74310077-09a9-42cb-9118-b6a72c9a3547" />
                                                          Figure 10.2: Homepage

<img width="592" height="306" alt="image" src="https://github.com/user-attachments/assets/175bd991-f86c-49cc-a7d3-ff4079935494" />
                                                          Figure 11: The AbuseIPDB Search Field


- 	Reviewing the IP details, including the number of abuse reports, categories of abuse (such as hacking, spam), last reported date, and country of origin, the results returned in the search shows show that the IP address was found in the database.
- 	The IP address has been reported 6,531 times from 730 distinct sources and the confidence of Abuse is rated 100%. 
 	Abusive activity associated with the IP address was first reported on November 21, 2020 and the abusive activities from the IP address are still ongoing.

  PART C: Reviewing a Domain with Cisco Talos Intelligence
  
- 	Given the fact that, threat hunting involves proactively searching for malicious events and activities within an environment to uncover ongoing cyberattacks, I believe that every Security Analyst must depend on communications with intelligence groups, creating the room to respond quickly and effectively to mitigate threats.
- 	Therefore, I decided to explore Cisco Talos Intelligence platform to investigate suspicious domain domains as Ioc.

Step 1

 	I opened a new tab
  
Step 2

 	In the address bar, I typed in https://talosintelligence.com/ 

<img width="564" height="291" alt="image" src="https://github.com/user-attachments/assets/aff3202a-f062-4d5c-8a06-57df8b126490" />
                                                         Figure 12: Homepage 

Step 3

 	In the search field, I entered a suspicious domain as www.example.com and pressed Enter
<img width="514" height="265" alt="image" src="https://github.com/user-attachments/assets/f275832e-0f99-412f-bb74-af303eca9fa6" />
                                                        Figure 13: Returned Results

The returned results showed several IP addresses associated with Hostname. The email reputation is rated poor.

##Results

I have learned the following:

- 	Detected and reviewed IoC as file hash, ip address, and domain name.
- 	Reviewed a file hash using VirusTotal, to determine file type, size, detection results, and associated malware family. The use of MalShare was unsuccessful due to an indefinite suspension of the platform after losing their host provider.
- 	Assessed an IP address through AbuseIPDB to evaluate its reputation, number of abuse reports, categories of abuse, and origin.
 	Investigated a domain using Cisco Talos Intelligence to examine reputation score, web category, related IPs, historical data, and security alerts.

##Further Research

Malicious URLs can be obtained from urlhaus.abuse.ch/ for further investigation and analysis. The database contains dozens for malicious URLs for testing purpose.

<img width="398" height="205" alt="image" src="https://github.com/user-attachments/assets/aa6f1696-383c-4511-9b05-c5fb5bb3ce80" />
                                                       Figure 14: Returned Results
                                                       

##Upcoming Additional Tasks:

- 	Find a suspicious URL or phishing link online (ensure it's legal and ethical to analyze) and then submit the URL to VirusTotal and interpret the scan results.
- 	Generate hash values (MD5, SHA-1, and SHA-256) for files using various tools and then submit these hash values to VirusTotal and observe how the platform associates different file instances with the same hash.
- 	Identify a file that is flagged as a false positive by an antivirus engine on VirusTotal.
- 	Identify patterns or changes in the behavior of a file or URL over time.









