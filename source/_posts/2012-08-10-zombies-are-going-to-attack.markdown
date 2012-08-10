---
layout: post
title: "Zombies are going to attack"
date: 2012-08-10 16:16
comments: true
categories: 
---

This guide demonstrates how you can constantly report your computer's internal 
and external IP address to a file in your Dropbox. 

Step 1:
=============
Create a text file which has the following cronjobs:
{% codeblock %}
*/5 * * * * curl -s http://checkip.dyndns.org | sed 's/[a-zA-Z/<> :]//g' > ~/Dropbox/IPAddresses/macbookair13/ip.txt
*/5 * * * * sh ~/Dropbox/crons/mba13/ifconfig.sh
{% endcodeblock %}

