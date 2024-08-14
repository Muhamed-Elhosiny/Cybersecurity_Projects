
## Basic Security Monitoring System with ELK Stack on Linux

## Project Description:
Set up a basic Security Information and Event Management (SIEM) system using the ELK Stack (Elasticsearch, Logstash, Kibana) on a Linux system. This project will involve configuring Elasticsearch for log storage, Logstash for log processing, and Kibana for visualization.

## Steps to Set Up Basic Security Monitoring

1. Install the ELK Stack

1.1 Install Elasticsearch

•	Download and install the Elasticsearch package:

![image](https://github.com/user-attachments/assets/ce1b1aa8-ba0a-4757-8e25-b430372faa45)

## Reinstall Elasticsearch: 

Because the Elasticsearch is not installed, I tried reinstalling it:

![image](https://github.com/user-attachments/assets/cf229ed0-0ee7-40a2-8e82-e31528da7a24)

•	Start and enable the Elasticsearch service:

![image](https://github.com/user-attachments/assets/a36bbbc5-2abb-4d62-a909-35924ffc72de)

•	Verify Elasticsearch is running:

![image](https://github.com/user-attachments/assets/2f54645d-a09c-4c6a-9d13-1a6f613a451c)

## 1.2 Install Logstash

•	Download and install the Logstash package:

![image](https://github.com/user-attachments/assets/2b812141-3329-40e1-ae4b-e5c5d7d6f861)

## Reinstall Logstash: 

![image](https://github.com/user-attachments/assets/756ebecf-56d8-40b0-8c22-f4406d08f7e9)

•	Start and enable the Logstash service:

![image](https://github.com/user-attachments/assets/5643f2a8-e579-41b0-a806-7169915f8134)

## 1.3 Install Kibana

•	Download and install the Kibana package: 

![image](https://github.com/user-attachments/assets/fe90d8b5-a0e7-4217-8c3d-dacdea9c7023)

![image](https://github.com/user-attachments/assets/0976f6c7-017b-4280-84bc-9af4254da4fd)

•	Start and enable the Kibana service:

![image](https://github.com/user-attachments/assets/a8daf505-7e37-4445-b488-fc95e6e6be4e)

Access Kibana: Once Kibana is installed and running, you can access it via your web browser at:http://localhost:5601.

![image](https://github.com/user-attachments/assets/0eb67f17-c410-4d73-931c-106068b34564)

## 2. Configure Logstash

   •	I Created a configuration file for Logstash:

   sudo nano /etc/logstash/conf.d/logstash-simple.conf

   •	I Added the following configuration to collect logs from a file and send them to Elasticsearch:

   ![image](https://github.com/user-attachments/assets/61f37961-b595-466d-9ea0-ea478695dae6)

  ## 2.2 Restart Logstash

  •	Restart Logstash to apply the new configuration:

# sudo systemctl restart logstash

## 3. Access and Use Kibana

3.1 Configure Index Patterns in Kibana

•	Open Kibana in your web browser at http://localhost:5601.

•	Go to Management > Stack Management > Index Patterns > Create Index Pattern.

•	Enter syslog-* as the index pattern and select the default time field (@timestamp).

## 3.2 Create Basic Dashboards

•	Go to Discover to view the logs that are being indexed.
•	Create visualizations and dashboards to display your log data by navigating to Visualize Library and Dashboard.
## 4. Analyze and Document

## 4.1 Review Captured Logs
•	In Kibana’s Discover tab, review the logs collected from /var/log/syslog.

•	Use filters and search to find specific log entries and patterns.

## 4.2 Document Your Findings

•	Write a brief report summarizing the setup process.

•	Include screenshots of your Kibana dashboards and any interesting findings from the log analysis.

## Tools Used

•	Elasticsearch: Stores and indexes log data.

•	Logstash: Processes and sends logs to Elasticsearch.

•	Kibana: Visualizes log data and provides dashboards.

•	Log Files: /var/log/syslog used for demonstration.

## Conclusion
This project provides a foundational introduction to setting up and using the ELK Stack for basic log management and visualization. By following these steps, you’ll gain hands-on experience with configuring Elasticsearch, Logstash, and Kibana, as well as understanding how to collect and analyze logs effectively. This simplified approach is ideal for entry-level experience and builds a solid foundation for more advanced SIEM configurations in the future.






   













