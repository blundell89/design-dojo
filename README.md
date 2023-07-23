# Brief

Our system processes payments to recipients in different countries. To do that we need to integrate our system into multiple different banking systems. A manual version of this process would be as follows...

A user in our system exports a batch of payment requests (a payment is simply "please pay $120 to Fred Bloggs, account number X, ABA code Y").

This batch of payments is all for a single bank. The user logs into that banks system, issues a money transfer for each payment in the batch and then marks that payment as complete in our system.

Some banks may have an API we could call - these might be "send a file over SFTP and check back later", "Call a SOAP method" or "send an HTTP POST request and we'll POST a callback".

# Exercise

Assuming that we would like to replace the manual upload and reconciliation, how would you design a mechanism to automate this process?

# System Design Overview

![system-overview](system-overview.png)