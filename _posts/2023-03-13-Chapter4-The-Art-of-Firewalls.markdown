---
layout: page
title:  "Chapter 4/ The Art of Firewalls and Rules"
date:   2023-03-13 22:34:00 -0500
categories: update
---

# Learning the Art of Firewall Rules

As I continue to learn more and more about the evils that try and do us harm, I’ve learned that securing your servers from malicious entities 
is of utmost importance. Firewalls provide a shield against unauthorized access and attacks, and one such tool in our arsenal is UFW (Uncomplicated Firewall). 
This mystical front-end for IPTables grants us the power to easily manage firewall rules through simple commands. In order to gain practical experience and 
valuable skills for my CySA+ studies, I have devised several scenarios to create powerful firewall rules. Join me on this adventure as we explore the realm 
of UFW and protect our servers from harm!

# Scenario 1: Allowing HTTP and HTTPS Traffic

The first scenario we'll cover is allowing HTTP and HTTPS traffic. To do this, run the following commands:
  sudo ufw allow http
  sudo ufw allow https
  
The above commands will allow traffic on HTTP and HTTPS ports. You can verify the rules have been added by running:
  sudo ufw status verbose

This command should output the following:
  Status: active

  To                         Action      From
  --                         ------      ----
  80/tcp                     ALLOW       Anywhere                  
  443/tcp                    ALLOW       Anywhere                  

# Scenario 2: Allowing SSH Access from a Specific IP Address

The second scenario we'll cover is allowing SSH access from a specific IP address. This is useful when you only want to allow SSH connections from a 
trusted source. To do this, run the following command:
  sudo ufw allow from 192.168.1.100 proto tcp to any port 22

The above command allows SSH traffic from IP address 192.168.1.100. You can verify the rule has been added by running:
  sudo ufw status verbose

This command should output the following:
  Status: active

  To                         Action      From
  --                         ------      ----
  22/tcp                     ALLOW IN    192.168.1.100

# Scenario 3: Allowing SMTP Traffic
The third scenario we'll cover is allowing SMTP traffic. SMTP is used for sending email messages between servers. To allow SMTP traffic, run the following 
commands:

  sudo ufw allow proto tcp from any to any port 25
  sudo ufw allow proto tcp from any to any port 465

The above commands allow traffic on port 25 and port 465. You can verify the rules have been added by running:
  sudo ufw status verbose

This command should output the following:
  Status: active

  To                         Action      From
  --                         ------      ----
  25/tcp                     ALLOW       Anywhere                  
  465/tcp                    ALLOW       Anywhere                  

# Conclusion
As I delved deeper into the art of CySA, I found that the basic firewall rules we learned using UFW were vital in solidifying my knowledge. With these 
newfound skills, I will venture forth into my homelab and craft a firewall of my own, honing my abilities and sharpening my expertise as a defender 
against the dark forces that threaten our servers. Each step I take brings me closer to my ultimate goal of becoming a SOC analyst, and with UFW as my 
guide, I will blaze a trail towards that destiny.
