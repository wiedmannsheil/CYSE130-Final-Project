Cybersecurity Automation and Monitoring System

- **Project Overview**

- The Cybersecurity Automation and Monitoring System is a comprehensive security toolset designed to automate essential security tasks. This system enables real-time detection of suspicious activity, system performance monitoring, and network traffic tracking. By automating these processes, organizations can enhance threat detection, reduce response time, and strengthen overall security posture.
  Key Features
    - Log File Analysis: Detects suspicious log entries related to unauthorized access, login failures, and errors.
    - System Monitoring: Tracks CPU and memory usage, raising alerts when thresholds are exceeded.
    - Alert Generation: Sends email notifications when suspicious activities are detected.
    - Security Automation: Uses Nmap to scan for open ports and services, identifying potential vulnerabilities.
    - Network Traffic Monitoring: Captures and logs IP traffic to identify unusual connections.


- **Installation Instructions**

    Prerequisites:
      Operating System: Linux (preferred) or Windows with Python installed.
      Required Python Libraries:
        - psutil for system performance monitoring.
        - smtplib for email alerts.
        - scapy for network traffic monitoring.
        - subprocess for running Nmap commands.
        - Note: Some scripts (e.g., Nmap) may require administrative/root privileges.

    Step-by-Step Setup:
      1 - Clone the Repository
        git clone https://github.com/yourusername/cybersecurity-automation.git
        cd cybersecurity-automation
  
     2 - Install Required Libraries
        pip install psutil scapy
  
     3 - System Permissions
        Linux: Ensure you have root/sudo privileges.
        Windows: Run PowerShell or Command Prompt as Administrator to avoid permission issues.

     4 - Set Up Environment Variables (for email alert configuration)
        export EMAIL_USER="your_email@example.com"
        export EMAIL_PASS="your_email_password"
  
- **Usage**
  1 - Log File Analysis
        Purpose: Detect suspicious activity in log files.
  How to Run:
    python scripts/log_analysis.py
  What it Does:

    Reads the system_log.log file.
    Identifies suspicious entries with terms like "failed" or "unauthorized."
    Outputs a report called summary_report.txt with total suspicious entries and details.
  
  2 - System Monitoring
        Purpose: Monitor CPU and memory usage.
  How to Run:
    python scripts/system_monitoring.py
  
  What it Does:

    Monitors system performance.
    Logs CPU and memory usage into performance_log.txt.
    Sends an alert if CPU usage exceeds 90%.
  3 - Alert Generation
        Purpose: Send email alerts for detected suspicious activity.

  How to Run:
  
    from scripts.alert_generation import send_alert

    send_alert(
      subject="ALERT: Suspicious Activity Detected",
      body="Suspicious activity was found in the system log. Check summary_report.txt for details.",
      sender_email="your_email@example.com",
      sender_password="your_email_password",
      recipient_email="security_team@example.com"
    )
  What it Does:

    Sends email notifications when suspicious activity is detected.
    Uses environment variables to keep email credentials secure.
  
  4. Security Automation (Nmap Scan)
        Purpose: Run Nmap scans to identify open ports and services on a system.
  
  How to Run:
  
    sudo python scripts/security_automation.py
  
  What it Does:

    Runs an Nmap scan of a target IP address.
    Saves the results to nmap_scan_results.txt.
  
  5. Network Traffic Monitoring
         Purpose: Monitor inbound and outbound network traffic.
     
  How to Run:
    sudo python scripts/network_traffic_monitoring.py

  What it Does:

    Captures network traffic using Scapy.
    Logs source and destination IPs to network_traffic_log.txt.
  
 ** Group Roles **

 

- Mohammed Zoolker (Moe)- Oversee the project, remind about deadlines, Submit the assignments, develop recovery plan, help mainly with Analysis and System requirements.  
- Abdulaziz Alsayegh, Patrick Tran- Create UML systems diagrams (for this project Demir is also helping with UML systems).  
- Mohammad Haider, Demir Ipek- Develop the Python scripts, fix the codes from the Detailed Instruction.
- Belal Raja- Perform Data Analysis and Machine learning task/ Write the report explaining the purpose of the scripts.







  
