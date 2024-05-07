### Ethical Hacking Technical Report
**Client:** Quantum Technology Corporation
**Date:** 2024-05-05
**Prepared by:** Jomel Abitan and Blessy Hyacinth Follosco</br>

**Executive Summary:** This report presents the results of ethical hacking conducted for Quantum Technology Corporation. The purpose of the assessment was to identify all possible weaknesses and vulnerabilities in the organization's network, web application, operating system, and other related components. A combination of penetration testing techniques with vulnerability scanning and social engineering was performed in order to find security risks. This report includes a summary of critical and high-risk vulnerabilities identified during the assessment, along with appropriate recommendations to address the existing issues. This aims to enhance the overall security within the organization.</br>

**Vulnerability Summary:**
1. **Network Infrastructure:**
    - **Critical:** Remote Code Execution (RCE) vulnerability (CVE-2023-12345) in the Apache Tomcat server (version 9.0.31), allowing unauthorized code execution with high privileges.

    - **High:** Insecure SNMP configuration on the network routers, allowing public access to sensitive network information.

    - **High:** Exposed Remote Desktop Protocol (RDP) on multiple servers without network-level authentication.

2. **Web Applications:**
    - **Critical:** Cross-site request Forgery (CSRF) vulnerability in [Web App X], permitting unauthorized transactions on behalf of authenticated users.

    - **High:** Directory traversal vulnerability in [Web App Y], enabling unauthorized file access.

    - **High:** Reflected Cross-Site Scripting (XSS) in [Web App Z], allowing injection of malicious scripts.

3. **Operating Systems:**
    - **Critical:** Unpatched operating systems (Windows Server 2012) with known vulnerabilities, exposing servers to malware and remote attacks.

    - **High:** Outdated third-party software (Adobe Acrobat Reader) on user workstations, which can be exploited for code execution.

    - **High:** Misconfigured security policies allowing standard users to access system-critical files.

4. **Wireless Networks:**
    - **High:** Weak wireless encryption (WPA) used in office networks, exposing traffic to potential interception and decryption.

    - **Medium:** Default SSID (Service Set Identifier) in use, making the wireless network easily identifiable.

5. **Social Engineering:**
    - **Critical:** Successful phishing attacks against several employees, resulting in the compromise of user credentials.

    - **High:** Lack of multi-factor authentication (MFA) on critical systems, increasing the risk of unauthorized access.

6.	**Database Security:**
    - **Critical:**  Lack of encryption for sensitive data in the Quantum, exposing confidential information in case of a data breach.

    - **High:** Default credentials on database management systems, permitting unauthorized access to the database.

7.	**Email Systems:**
    - **Critical:** SMTP relay open for external connections, allowing unauthorized users to send emails using the company's domain, potentially leading to spam or phishing.

     - **High:** Insecure email transmission protocols (non-TLS) in use, allowing potential interception of email traffic.

8.	**Network Segmentation:**
    - **Critical:** Lack of network segmentation, permitting unauthorized users to move laterally across the internal network, increasing the risk of data exfiltration or internal attack.

    - **High:** Insufficient access controls between different network segments, allowing broad access to sensitive areas.

9.	**Endpoint Security:** 
    - **High:** Antivirus software not installed on several user workstations, leaving them vulnerable to malware and viruses.

    - **High:** Unauthorized software installations allowed on endpoints, potentially introducing malicious software into the environment.

10.	**Backup Systems:**
    - **High:** Backups not encrypted, exposing sensitive data if backup media is lost or stolen.

    - **Medium:** Backup routines not properly scheduled, increasing the risk of data loss due to inadequate backups.

11.	**Physical Security:**
    - **High:** Unrestricted access to server rooms, allowing unauthorized physical access to critical infrastructure.

    - **Medium:** Lack of security cameras in sensitive areas, reducing the ability to monitor for unauthorized access or security incidents.

12.	**Monitoring and Logging:**
    - **Critical:** Lack of centralized logging, reducing the ability to detect and respond to security incidents promptly.

    - **High:** Insufficient monitoring of security events, increasing the risk of delayed detection of threats.

13.	**Development Practices:**
    - **High:** Insecure software development practices, such as hardcoding credentials in source code, exposing sensitive information.

    - **Medium:**  Lack of security testing in the development lifecycle, allowing vulnerabilities to be introduced into production systems.

14.	**Third-Party Services:**
     - **Critical:** Inadequate vetting of third-party vendors, increasing the risk of supply chain attacks.

    - **High:** Weak access controls for third-party services, allowing unauthorized access to sensitive data.

15.	**IoT Devices:**
    - **Critical:** Insecure IoT devices connected to the internal network, providing a potential entry point for attackers.

    - **High:** Default passwords on IoT devices, allowing easy unauthorized access and control of these devices. </br>

**Recommendations:**
1. **Network Infrastructure:**
    - **Patch Apache Tomcat** to the latest version to fix the RCE vulnerability.

    - **Secure SNMP** configurations by using strong community strings and restricting public access.

    - **Restrict RDP access** to authorized users only, with network-level authentication.
2. **Web Applications:**
    - **Implement CSRF protection with anti-CSRF tokens** to mitigate CSRF attacks.
    
    - **Harden input validation** to prevent directory traversal and XSS vulnerabilities.

    - **Conduct regular code reviews** to ensure security best practices are followed.

3. **Operating Systems:**
    - **Implement a patch management strategy** to regularly update and secure operating systems.

    - **Upgrade outdated software** to prevent exploitation of known vulnerabilities.

    - **Review security policies** to ensure restricted access to system-critical files.

4. **Wireless Networks:**
    - **Switch to WPA3 encryption** to secure wireless communications.

    - **Change the default SSID** to a unique, non-identifiable name to minimize potential attacks.

5. **Social Engineering:**
    - **Conduct regular security awareness** training to educate employees about phishing attacks and security best practices.

    - **Implement multi-factor authentication (MFA)** on critical systems to reduce the risk of unauthorized access.

6.	**Database Security:**
    - **Implement encryption for sensitive data** to ensure data protection even if a breach occurs.

    - **Change default database credentials** and enforce strong authentication mechanisms for database access.


7.	**Email Systems:**
    - **Close SMTP relay** to external connections to prevent unauthorized email usage.

    - **Implement email encryption protocols (TLS/SSL)** to secure email transmissions.

8.	**Network Segmentation:**
    - **Implement network segmentation** to isolate sensitive areas from general user access.

    - **Strengthen access controls** between different network segments to minimize the risk of unauthorized lateral movement.
9.	**Endpoint Security:**
    - **Install antivirus software** on all user workstations and ensure it's regularly updated.

    - **Restrict unauthorized software installations** on endpoints through endpoint management policies.

10.	**Backup Systems:**
    - **Encrypt backups** to protect sensitive data from unauthorized access.
    
    - **Establish regular backup schedules** and test backup restoration to ensure data integrity and availability.

11.	**Physical Security:**
    - **Restrict physical access** to server rooms and critical infrastructure to authorized personnel only.

    - **Install security cameras** in sensitive areas to monitor for unauthorized access or security incidents.

12.	**Monitoring and Logging:**
    - **Implement centralized logging** to improve security event tracking and incident response.

    - **Enhance security event monitoring** to ensure prompt detection and response to threats.

13.	**Development Practices:**
    - **Ensure secure development practices**, such as removing hardcoded credentials and using environment variables.

    - **Integrate security testing** into the development lifecycle to identify vulnerabilities before production deployment.

14.	**Third-Party Services:**
    - **Conduct thorough vetting** of third-party vendors to ensure they meet security standards.

    - **Strengthen access controls** for third-party services to prevent unauthorized access to sensitive data.

15.	**IoT Devices:**
    - **Secure IoT devices** by changing default passwords and ensuring they are updated with the latest firmware.

    - **Isolate IoT devices** from sensitive network segments to reduce the risk of unauthorized access. </br>

**Conclusion:** The results of the ethical hacking assessment have uncovered numerous critical and high-risk vulnerabilities in both the infrastructure and the applications used by Quantum Technology Corporation. It is highly recommended to take all of the measures mentioned above, as this would highly reinforce an organization's security level and reduce the chances of risks related to unauthorized access and data breaches.

</br>

**Signature:**
![](images/Picture5.jpg)  ![](images/Picture6.jpg) 




