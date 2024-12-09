# Initial-Access-Malicious Document Traffic

## Malicious Document Traffic
Based on the collected findings, we discovered that the attacker fetched the stage 2 payload remotely:

    We discovered the Domain and IP invoked by the malicious document on Sysmon logs.
    There is another domain and IP used by the stage 2 payload logged from the same data source.

## Investigation Guide
Since we have discovered network-related artefacts, we may again refer to our cheatsheet, which focuses on Network Log Analysis:

    We can now use Brim and Wireshark to investigate the packet capture.
    Find network events related to the harvested domains and IP addresses.
    Sample Brim filter that you can use for this investigation: _path=="http" "<malicious domain>"

Data Sources:

    Packet Capture
