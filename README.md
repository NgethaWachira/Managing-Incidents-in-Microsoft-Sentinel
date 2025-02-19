# Objective
To explain the process of triaging, investigating, and responding to incidents in Microsoft Sentinel, focusing on the steps involved in managing incidents, prioritizing them based on severity, using investigation tools (such as visualizations and timelines), assigning tasks, running automation rules, and collaborating with teams through Microsoft Teams. Emphasizing key actions like adjusting incident severity, tracking progress, handling tasks, investigating IPs, and ultimately responding to and closing incidents after taking necessary actions.

## Skills Learned
- Incident Management and Prioritization: Learned how to manage and view security incidents, adjust timeframes, assess and prioritize incidents based on severity, and modify severity levels when necessary to ensure critical incidents are addressed first.

- Gained expertise in investigating incidents by analyzing key details such as entities involved, tactics, techniques, IP addresses, and timelines. Use Sentinel’s investigation features, including visualizations, queries, and real-time log monitoring, to track activities and understand the scope of incidents.

- Task Assignment and Tracking: Developed the ability to assign and track tasks within an investigation, monitor progress, and ensure completion of required actions. Tasks can be marked off as completed once finished.

- Collaboration and Team Management: Used Microsoft Teams to create teams, collaborate on incidents, and coordinate responses. Share information and manage discussions to ensure efficient team-based decision-making.

- Automation and Playbook Execution: Understood how to run automated playbooks and create automation rules to streamline responses and alleviate manual tasks, improving future incident management.

- Incident Closure and Classification: Learned the process for closing incidents, assigning classifications, and ensuring all response actions have been completed and documented.

## Tools Used
<div>
<img src="https://img.shields.io/badge/-Microsoft%20Sentinel-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" alt="Microsoft Sentinel">
<img src="https://img.shields.io/badge/-Activity%20Log-a300cc?style=for-the-badge&logo=microsoft&logoColor=white" alt="Activity Log">
<img src="https://img.shields.io/badge/-Task%20Management-e68a00?style=for-the-badge&logo=microsoft&logoColor=white" alt="Task Management">
<img src="https://img.shields.io/badge/-Incident%20Timeline-3d3d29?style=for-the-badge&logo=microsoft&logoColor=white" alt="Incident Timeline">
<img src="https://img.shields.io/badge/-Playbooks-d98cb3?style=for-the-badge&logo=microsoft&logoColor=white" alt="Playbooks">
<img src="https://img.shields.io/badge/-Microsoft%20Teams-e0e0eb?style=for-the-badge&logo=microsoftteams&logoColor=white" alt="Microsoft Teams">
</div>

## Steps
- In  viewing and prioritizing incidents in Microsoft Sentinel, log in the Microsoft Sentinel portal, find and click on Threat Management in the left-hand pane, under Threat Management, select Incidents to view the list of active incidents. At the top of the Incidents page, you should see a filter option to adjust the time range for the incidents to help focus on recent and active threats. Click on each listed incident to preview a summary of the incident.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/cd35eba1c4a7ceac5035d623a01490ec21001dca/Images/Preview%20of%20the%20incidents%20details.PNG" width="700" />
</p>

- After previewing the incident summary, click on the View Details button to open the full details of the incident. Here you'll find specific events that triggered the incident, any alerts related to the incident, a timeline of actions and events that occurred. Assign ownership to yourself by clicking on the Unassigned button in the incident details view and select your name - this ensures that you are responsible for investigating and resolving the incident. 

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/a46af877da13215f7c72bb04599ebe24f3816e85/Images/Assign%20the%20incident%20to%20myself.PNG" width="700" />
</p>

- Prioritize Incidents Based on Severity, incidents are usually categorized as low, medium, or high based on their potential impact, there is also the option to edit the severity level if it is miscategorized. If you are actively working on the incident, you should update the Status to "Active" to indicate you’re investigating it. After reviewing the incident, break down the investigation into actionable tasks such as Analyzing logs and alerts, checking for compromised user accounts or systems, running scans for malware or malicious behavior, reviewing network traffic and firewall logs etc. Keep track of each assigned task and its progress, you might have an internal task management tool or an external one like ServiceNow to assign tasks and track completion.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/13318f76a56fa2f82bfd69a8a1228d8a50e6b097/Images/Creating%20tasks%20in%20investigation.PNG" width="700" />
</p>

- Once inside the detailed incident page, locate and click on the "Investigation" tab. Here we'll find visualization tools such as timeline views that can help us explore the relationships between entities, such as IP addresses. click on IP addresses in the incident or entity list. This will help you see the full scope of activity related to that IP which can be explored on a graph.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/c33b50b681e7eefe33ead3354de49b7e71e2aae3/Images/Incident_view%20details_investigate.PNG" width="340" />
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/c33b50b681e7eefe33ead3354de49b7e71e2aae3/Images/Related%20events%20in%20investiation.png" width="300" />
</p>

- You can also use KQL queries (Kusto Query Language) to run specific queries that help retrieve related events. These queries can search logs for activities related to the IP. Adjust the query to search for the IP in relevant tables (e.g., SecurityEvent, AzureActivity, Syslog, etc.) depending on the context of the incident.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/d72d0d80bf16d8bf0a953e5a6b4066eb1861ffc5/Images/Events%20related%20to%20that%20IP.PNG" width="700" />
</p>

- Review the incident timeline in the overview tab, the timeline section will display a comprehensive view of all the activities related to the incident. It will help you visualize how the incident unfolded in chronological order, which is essential for understanding the attack's progression and identifying any gaps or missed alerts.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/d76ee143535a41c1df56dbcf64d73b870c5669a1/Images/Timeline%20of%20various%20events.PNG" width="700" />
</p>

- Access the incident's action button. Once you are inside the incident details page, locate the incident action button with a drop down arrow, it provides options for responding to and managing the incident. We have the option to run playbooks and automated workflows that can help you respond to incidents, or create automation rules to allow us to define actions that automatically take place in response to incidents, alerts, or form a team to discuss and plan a response.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/69a18166d7708568f02ccce095c9d0cce1f3ae1b/Images/Responding%20to%20an%20incident.PNG" width="700" />
</p>

- If you've decided to go with the options of collaborating with the team using Microsoft Teams, then create a dedicated channel in Microsoft Teams, invite all necessary team members to this channel, link to the incident in Sentinel (you can use a URL to the incident or share the summary), complete all tasks and ensure the incident is fully investigated, close the incident by returning to Microsoft Sentinel, and go to the specific incident that has been resolved, change the Incident Status to "Closed". Assign an appropriate classification to the incident - this is where you categorize the nature of the incident e.g. False Positive, True positive, undetermined etc. Add notes or a summary of the incident closure details, this can include what was done, how the issue was mitigated, and any lessons learned.

<p align="center">
  <img src="https://github.com/NgethaWachira/Managing-Incidents-in-Microsoft-Sentinel/blob/033d145f9372e02845449b9948851eccbd951b5b/Images/Closing%20an%20incident.PNGG" width="700" />
</p>










