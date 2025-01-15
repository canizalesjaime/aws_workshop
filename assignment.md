# Project 1 - Prototype a ChatBot that queries an AWS service

## Learning Objectives
*	Compare different core cloud services and explain how they are used, specifically relating to Compute, Storage, Networking, Database, Security (IAM).
*	Describe the practice of monitoring the health of systems and the impact on application performance, e.g., CPU, Memory, Network I/O, and Disk I/O metrics.
*	Write code to satisfy requirements using fundamental concepts: data structures, conditionals, loops, variables, functions, and/or object-oriented principles.
*	Relate the concept of virtualization to cloud computing, explaining the functionality of resources delivered through the cloud.
*	Demonstrate ability to communicate with stakeholders of different technical depths.

|           What is the   general business problem you’ll solve?                                                                                                                                                                                                                                                                                                                                                                                                                                                            |           Why is it important to the business   to solve?    |           What is the solution and how could   the solution be convincingly presented?                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     You   work at a SaaS company that provides its customers with access to a SaaS   solution.     A large   team of Customer Success Managers (CSMs) have been pinging engineering   regularly to learn about upcoming expected downtime for a core service hosted   on AWS.       Despite   documentation and updated SLAs, the CSMs continue to do it.      It's a   distracting set of messages for Engineers and Engineering Leadership – who   rarely answer within the agreed upon SLA (up to 1 business day).     | **Improved Efficiency:** An automated solution to this problem can provide a self-service way for the customer success teams to check the status of service themselves. <br>**Engineer Productivity:** Frequent interruptions from the customer success team can be disruptive and impact their productivity. A solution to this will help engineers stay focused on their core responsibilities.<br>**The key metric engineering will look to reduce with a solution:** Inquires that gets automatically tracked in Discord. **Success will be defined as follows:**<br>1.	Metric: Number of service status inquiries over time.<br>2.	Before Automation: 50 inquiries per day (constant).<br>3.	After Automation: 30 inquiries per day (declining).<br>                                                             |     Engineering   leadership has tasked you with prototyping an automated Discord bot that can   serve data from the service – hosted on EC2 – that CSMs are constantly asking   about.      An   automated solution will allow Engineering team members to focus on   higher-value tasks, leading to increased efficiency and productivity. In   contrast, messaging engineering may require constant back-and-forth   communication and can be time-consuming.     It   will also allow for reduced the risk of human errors – from misinterpretation   to copy and paste errors - which can lead to costly mistakes and rework.           |

## Project Requirements
### Languages/Technologies: 
*	Python, including – but not limited to - the following libraries:
    *	Discord 
    *	EC2_metadata
    *	psutil
*	Discord
*	AWS

#### You’ll be evaluated against 5 deliverables as described in the rubric below: 
*	A Live Discord Server
*	A live EC2 server in AWS
*	A .py file using the EC2_metadata library and following proper security practice
*	Live, updated Discord Server that uses code from .py file and serves data from EC2 server
*	4-5 sentence summary describing the prototype for Engineering Leadership

|     Requirements                                                                           |     Deliverable(s)                                                                                 |     0   – Incomplete / Missing                                                                                                                                                                                                                                                                                                             |     1   – Does not satisfy requirements                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |     2   - Satisfies Requirements                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |     3   – Exceeds Requirements                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     1. Discord server input/output is live.                                                |     Live Discord Server                                                                            |     The student's submission lacks essential components for a   functional Discord server and text input response.     The Discord server may be set up but does not respond to   the "hello world" message as expected.     There are missing or incomplete configurations, such as   token setup, event listeners, or response logic.    |     The Discord server does not respond to the "hello   world" message with the expected "hello" reply; the server   experiences technical issues or downtime, making it unresponsive to any   input.                                                                                                                                                                                                                                                                                                      |     Discord server is able to receive “hello world” message   and reply back with “hello” back.                                                                                                                                                                                                                                                                                                                                                                                                        |     “Satisfies Requirements” plus:     Discord server is able to reply to at least one other   input besides “hello world” (ie - handle for other string text);      The submission includes comprehensive documentation that   explains the server's functionality, key configurations, and response logic;      the server handles errors, providing informative   responses in case of unexpected input or issues.                                                                                                                                                                                                                                                                                                                                                       |
|     2.  Able to   retrieve information about live EC2 server.                              |     EC2 server in AWS.           .py file using the EC2_metadata library                           |     .py file lacks any attempt to interact with an EC2   server.     The .py file returns information about the EC2 server,   but the output is unstructured and difficult to interpret, lacking proper   formatting or labeling.                                                                                                          |     EC2 server is live and able to field responses from a   client, but the .py file fails to establish a connection with the designated   EC2 server and cannot receive responses from it.     Key information, such as CPU utilization, IP address,   region, or availability zone, is missing, incorrect, or inconsistent with the   actual state of the EC2 server.     The program exhibits performance issues, such as slow   data retrieval, high resource usage, or other inefficiencies.          |     EC2 server is live and able to field responses from a   client.     The .py file successfully establishes a connection with   the designated EC2 server and is able to receive responses from it.     The .py file, when executed, accurately retrieves and   displays the following information about the EC2 server:     - AWS region where the EC2 server is hosted.     - Availability zone within the region where the EC2   server is located.                                               |     “Satisfies Requirements” plus:     The .py file, when executed, accurately retrieves and   displays the following information about the EC2 server:     - CPU utilization (as a percentage).     - IP address (public or private, as specified).     The program includes error handling to account for   potential issues, such as server unavailability or connection problems,   providing informative error messages when necessary.     Includes comprehensive documentation that explains the   purpose of the .py file, its usage, and the steps taken to retrieve the   specified EC2 server information.     The solution is designed with scalability in mind,   ensuring that it can be adapted for use with multiple EC2 servers if   necessary.            |
|     3. Script using EC2_metadata library is executable in bot   and live in EC2 server.    |     Live, updated Discord Server that uses code from .py file   and serves data from EC2 server    |     Discord server any attempt to interact with an EC2   server.     The server returns information about the EC2 server, but   the output is unstructured and difficult to interpret, lacking proper formatting   or labeling.                                                                                                            |     EC2 server is live and able to field responses from a   client, but the Discord server fails to establish a connection with the   designated EC2 server and cannot receive responses from it.     Key information, such as CPU utilization, IP address,   region, or availability zone, is missing, incorrect, or inconsistent with the   actual state of the EC2 server.     The server exhibits performance issues, such as slow data   retrieval, high resource usage, or other inefficiencies.     |     Discord server responds to “Tell me about my server!”   with the following information about the EC2 server:     - AWS region where the EC2 server is hosted.     - Availability zone within the region where the EC2   server is located.                                                                                                                                                                                                                                                         |     “Satisfies Requirements” plus:     Discord server responds to “Tell me about my server!”   with he following information about the EC2 server:     - CPU utilization (as a percentage).     - IP address (public or private, as specified).     The Discord server includes error handling to account for   potential issues, such as server unavailability or connection problems,   providing informative error messages when necessary.     Includes comprehensive documentation that explains the   purpose of the Discord server, its usage, and the steps taken to retrieve the   specified EC2 server information.     The solution is designed with scalability in mind,   ensuring that it can be adapted for use with multiple EC2 servers if   necessary.    |
|     4. Security best practices are followed                                                |     .py file following proper security practices                                                   |     AWS credentials and/or Discord tokens are hard coded.                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |     AWS credentials and Discord tokens are moved and stored   as and called from environmental variables.                                                                                                                                                                                                                                                                                                                                                                                              |     n/a                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|     5. Summary for Engineering Leadership                                                  |     4-5 sentence   summary describing the prototype for Engineering Leadership                     |     The summary is missing key elements, such as the problem   statement, solution description, what worked/didn't work, and what they would   do differently next time.     There is a lack of clarity in the summary, making it   difficult to understand the project's context and objectives.                                          |     The summary includes the required elements but lacks   detail or coherence.     The problem statement and solution description are vague   and do not effectively convey the project's purpose.     There is little to no reflection on what worked and what   didn't work.     The summary lacks critical thinking and fails to provide   a clear understanding of the project's outcomes.                                                                                                            |     The summary provides a clear and concise problem   statement, outlining the issue faced by the SaaS company and its customers.     The solution description is well-articulated, explaining   how the Discord bot prototype addressed the problem effectively.     It briefly mentions what worked and what didn't work   during the project, offering some insights into the decision-making process.     The summary demonstrates an understanding of the   project's context and objectives.    |     The summary offers a comprehensive and well-structured   explanation of the problem, making it clear why the project was necessary.     The solution description is detailed and highlights the   technical aspects of the Discord bot prototype's design and implementation.     It provides a thoughtful and insightful analysis of what   worked well and what didn't work, showing a deep understanding of the   project's challenges.     The "What would you do differently next time"   section displays critical thinking and suggests innovative ideas for future   improvements.     The summary engages the reader and effectively conveys   the project's significance and achievements.                                                                    |

Student Resources and Notes to Get Started
*	Follow the instructions provided by your professor to access AWS Credits and accounts before beginning the project.
*	Standing up an EC2 instance: video:
    *	Official AWS Docs: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html
*	In terms of EC2 server, select Instance Type: t2.micro with Ubuntu or Amazon Linux (your choice)
*	Discord developer docs: https://discord.com/developers  
*	Discord bot in Python: https://realpython.com/how-to-make-a-discord-bot-python
*	Discord.py Quick Start to respond to messages: https://discordpy.readthedocs.io/en/stable/quickstart.html
*	Ec2-metadata repo: https://github.com/adamchainz/ec2-metadata#ec2metadatasessionnone 
*	Psutil repo: https://psutil.readthedocs.io/en/latest/
*	Infrastructure teardown - Do not forget to tear down your EC2 instance once you complete the exercise
*	Example discord bot screenshot:<br><img src="./Picture1.png" /><br>



### Summary, Step-by-Step Solution:
1.	Create an EC2 Server with Instance Type: t2.nano and Amazon Linux
2.	SSH into the instance
3.	Python3 should already be installed. Install pip using sudo dnf install python3-pip
4.	Copy the bot.py into the instance
5.	pip3 install python-dotenv discord.py ec2-metadata psutil
6.	Create a Discord server and bot. Add the bot to the server. Make sure Privileged Gateway Intents > Message Content Intent is turned on.
7.	Complete .env file with the Discord bot token.
8.	Run python3 bot.py
9.	Send ‘Tell me about my server!’ in any channel on the Discord server where the bot was added.



# Notes ///////////////////////////////////////////////////////////////////////
1. psutil is a cross-platform library for retrieving information on running 
processes and system utilization (CPU, memory, disks, network, sensors)

2. ec2_metadata is An easy interface to query the EC2 metadata API (version 2), 
with caching.