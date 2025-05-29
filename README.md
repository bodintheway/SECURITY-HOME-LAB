# SECURITY-HOME-LAB
Building my own cybersecurity home LAN environment.


To begin my cybersecurity home lab project, I first ensured that virtualization was enabled in my system's BIOS. I then installed Oracle VirtualBox, a free and open-source hypervisor, to host and manage my virtual machines. Following Ben Heater's comprehensive guide on building a security lab in VirtualBox, I planned the network architecture and set up the initial virtual machines, starting with pfSense as the firewall and router for the lab environment


Installing the VirtualBox Extension Pack
After installing Oracle VirtualBox, it's highly recommended to install the VirtualBox Extension Pack to enhance functionality and improve support for USB 2.0/3.0 devices, VirtualBox RDP, PXE boot for Intel cards, and other features.

To install it:

Download the latest version of the Extension Pack from the official VirtualBox website.
![image](https://github.com/user-attachments/assets/1c9fbda1-da6d-4578-bde1-f8c43f2b50ae)


# Building a pfSense VM for Our VirtualBox Cyber Range

Plan Your Network First
Always plan your network before building your lab. It’s easier to design it right from the start than to fix it later—especially if you plan to expand.

[Download pfSense](https://www.pfsense.org/download/?ref=benheater.com)

![image](https://github.com/user-attachments/assets/c1501b79-7b33-4c72-b276-1c1795e7fce5)

![image](https://github.com/user-attachments/assets/603280da-2b80-4e5b-a985-0a60f4f11ba9)

![image](https://github.com/user-attachments/assets/b9f14a13-ec03-4b7d-9310-0404b06d9e51)

You can create an account or download pfSense without one. Creating an account helps you get updates and support. To create an account, go to the pfSense website, sign up with your email and a password, and verify your email.


Then, create the VM in VirtualBox as shown below.

![image](https://github.com/user-attachments/assets/fdae28a9-8012-4abb-8937-b46ac18e791f)

Keep the hardware settings simple. After setting up the VM, do not start it yet.


# Customize the VM

![image](https://github.com/user-attachments/assets/0639e58d-0a46-405f-9009-dff7bd86c4ae)
![image](https://github.com/user-attachments/assets/18788fdc-9cbd-4936-8c92-620425e66a24)
![image](https://github.com/user-attachments/assets/e21b165f-2198-4409-98ea-dc048b0d9225)

Move Hard Disk above Optical and disable Floppy

# Configure the Network Interfaces
 ## Adapter 1: WAN
![image](https://github.com/user-attachments/assets/781471b7-455d-4636-85b7-6837c9eae3db)

 ## Adapter 2: LAN
![image](https://github.com/user-attachments/assets/b96111fb-0731-490d-adb6-af9e9e583803)

 ## Adapter 3: ISOLATED
![image](https://github.com/user-attachments/assets/0af63124-1d44-4396-b925-817162f1a3e8)

## Adapter 4: AD_LAB
![image](https://github.com/user-attachments/assets/c25d7159-f95e-4ba7-b2e9-4f28b6d83749)

After this just click ok.
Customize the VM as needed. After configuring it, go ahead and start the VM.

![image](https://github.com/user-attachments/assets/eff12c39-3a9c-4990-9e0e-a20161087bb2)
![image](https://github.com/user-attachments/assets/2e48c97c-5ed2-4312-afc5-3e02f1665f2e)
![image](https://github.com/user-attachments/assets/e52d24d6-d3e2-4b31-b00d-951aca0da6ee)
![image](https://github.com/user-attachments/assets/46a2cc61-8e90-4c30-91bf-ad289279398f)
![image](https://github.com/user-attachments/assets/2233a1b0-fb62-4802-8752-aa5880868ce0)
![image](https://github.com/user-attachments/assets/d5daaa30-db8d-4624-9d18-7a4125099193)
![image](https://github.com/user-attachments/assets/cff9d08c-ff5d-4026-a1b8-e2472d831e2f)
![image](https://github.com/user-attachments/assets/837d5d0e-429f-47cd-a734-848b7a3bbdbe)
![image](https://github.com/user-attachments/assets/f781bfd1-b3c7-4d0a-9889-1416d8c5c5b2)
![image](https://github.com/user-attachments/assets/bf025a35-980e-4e29-bfa9-fb2838e73a10)
![image](https://github.com/user-attachments/assets/7f69292f-80cd-478f-bcfc-37f5852e33d9)
![image](https://github.com/user-attachments/assets/ea164b42-05c2-4011-b010-32eb5b9f2e8e)

Now, we need to configure pfSense.

now enter the wan interface

![image](https://github.com/user-attachments/assets/4d5d1228-8f68-4d19-8a27-dad6d4af85fa)
then the lan, isolated and ad-lab

![image](https://github.com/user-attachments/assets/80eae1a9-e088-45cb-8e66-676879a5b308)
![image](https://github.com/user-attachments/assets/7eb3a532-bb93-4bd7-8fcf-6085f9293693)
![image](https://github.com/user-attachments/assets/aa9b5dbf-18d1-4a7b-9f0d-b55c0c8ee5da)
![image](https://github.com/user-attachments/assets/f6225851-166f-4458-a0c8-8acbc25dd744)



![image](https://github.com/user-attachments/assets/37a9cb6b-756b-4e17-8d64-956a3617162e)
![image](https://github.com/user-attachments/assets/019a33bb-33ef-436c-98d5-49abfe25820c)

![image](https://github.com/user-attachments/assets/f08e2e97-cb8a-439b-bb49-3f5a684b31a9)
Enter 'n' to configure the address statically
![image](https://github.com/user-attachments/assets/a452dd41-5b59-4279-879e-6bb49a95d990)
the network address

![image](https://github.com/user-attachments/assets/1f4cd1df-42a7-4ef1-b89f-d963ad811843)
the subnet mask bits

enter then n

![image](https://github.com/user-attachments/assets/dc18603c-505c-409f-aa62-7a2b53efc137)
press enter


![image](https://github.com/user-attachments/assets/90572f75-9c9b-4458-ae0e-991991c2efa1)
press y

![image](https://github.com/user-attachments/assets/2dc02107-d8f5-461b-8504-7fd49fa0c7b7)
the start and end range


After doing the same with the AD-lab, isolated, and LAN networks, the final setup should look like this:
![image](https://github.com/user-attachments/assets/b636c329-6cdf-4a54-a86f-f877b11666d3)



# Importing Kali from Official Sources
 Go to https://kali.org/get-kali/.

Click Virtual Machines.

Click the Download icon. The file is large, so it may take some time to download.

Open VirtualBox.

Extract the downloaded .7z file to get the .vbox and .vdi files.

Rename the folder containing these files if you want.

Move (Cut and Paste) this folder to your VirtualBox VMs directory:

C:\Users\<YourUsername>\VirtualBox VMs\

Paste it here alongside your pfSense VM folder.

In VirtualBox, click Tools → Add, then select the Kali .vbox file.

❗ Do not start the VM yet!

Right-click the Kali VM, choose Settings.

Attach the Kali VM to the pfSense LAN network.

(Optional) Increase RAM under System settings if you want.

Click OK.

Now start the Kali VM.

Default login:

Username: kali

Password: kali

⚠️ Please change the password as soon as you log in.

To check your network, open the terminal and run ip a. You should see an IP like 10.0.0.11 assigned by pfSense’s DHCP server.

After that just type ip address in the terminal

![image](https://github.com/user-attachments/assets/9e378cce-b262-4ff0-9325-0ff6d956ef6b)


# Configure the PfSense firewall

Now open your terminal in Kali and type this https://10.0.0.1/

![image](https://github.com/user-attachments/assets/0750a24f-2f7b-4b06-97f2-4f5724b25342)
![image](https://github.com/user-attachments/assets/2e3a0ab1-9cf3-4e80-ae45-4a5e871a3d51)
![image](https://github.com/user-attachments/assets/d8641b14-6f23-489a-ae09-0980893781d0)
 accept

 The default credentials are Username: admin  Password: pfsense


## Configure the Interfaces
Isolated Interface
Choose OPT1

 ![image](https://github.com/user-attachments/assets/8dfe56d3-b6ca-4dd5-8168-5663dc4e15a2)

 for the AD_LAB Interface
 Choose OPT2 AND RENAME IT TO AD_LAB
 
\\\

Optimize the DNS Resolver Service
Go to Services > DNS Resolver

![image](https://github.com/user-attachments/assets/8adef5ae-f0a9-40c6-95b4-7ccb26ec666b)

![image](https://github.com/user-attachments/assets/761caf0d-9d97-4915-9774-a1e5d320ea2e)

![image](https://github.com/user-attachments/assets/ee25aea5-eb52-47f1-919a-9394dbac832d)

Give Kali a Static DHCP Lease
Go to Status > DHCP Leases ( A DHCP lease is the temporary assignment of an IP address to a device by a network server. )

![image](https://github.com/user-attachments/assets/4eb71f2b-59b8-46d7-9cb3-6a67407e9eb5)

![image](https://github.com/user-attachments/assets/dd45e0e7-56a9-424d-a2c0-247f7d7d8272)
set it to 10.0.0.2 then click save and apply.


# Configure the Firewall Rules
Create an alias for RFC1918 to reference all private IPv4 address spaces in future firewall rules.

Go to Firewall > Aliases

Click Add

Create the alias for RFC1918 networks

Click Save
![image](https://github.com/user-attachments/assets/129ecf8e-3c3a-4c03-999a-5fe8b2bdec54)
![image](https://github.com/user-attachments/assets/6b310a77-54d2-4aee-9785-d5b2cea93c2d)

# Firewall Rule Configuration Guide

This document describes how to configure firewall rules for the `LAN`, `ISOLATED`, and `AD_LAB` interfaces to enforce segmentation and control traffic. Copy this into your GitHub README or documentation.

---

## LAN Interface Rules

**Goal:** Block LAN devices from accessing WAN subnets

1. Navigate to **Firewall > Rules > LAN**.  
2. Click **Add** to create a new rule.  
3. Configure the rule:
   - **Action:** Block  
   - **Interface:** LAN  
   - **Address Family:** IPv4 + IPv6  
   - **Protocol:** Any  
   - **Source:** Any  
   - **Destination:** WAN net (or specify WAN subnet ranges)  
   - **Description:** Block access to any on same network as host OS  
4. Click **Save**, then **Apply Changes**.

---

## ISOLATED Interface Rules

**Goal:** Allow DNS and access to Kali VM, block everything else

1. Navigate to **Firewall > Rules > ISOLATED**.  
2. **Rule 1:** Allow DNS lookups  
   - **Action:** Pass  
   - **Interface:** ISOLATED  
   - **Address Family:** IPv4  
   - **Protocol:** UDP  
   - **Source:** ISOLATED net  
   - **Destination:** ISOLATED address (gateway)  
   - **Destination Port Range:** From 53 (DNS) to 53 (DNS)  
   - **Description:** Allow DNS lookups to the default gateway  
   - Click **Save** and **Apply Changes**.  
3. **Rule 2:** Allow access to Kali VM  
   - **Action:** Pass  
   - **Interface:** ISOLATED  
   - **Address Family:** IPv4  
   - **Protocol:** Any  
   - **Source:** ISOLATED net  
   - **Destination:** Alias = Kali  
   - **Description:** Allow packets to Kali VM  
   - Click **Save** and **Apply Changes**.  
4. **Rule 3 (Final):** Block all other traffic  
   - **Action:** Block  
   - **Interface:** ISOLATED  
   - **Address Family:** IPv4 + IPv6  
   - **Protocol:** Any  
   - **Source:** Any  
   - **Destination:** Any  
   - **Description:** Block access to everything  
   - Click **Save**, then **Apply Changes**.

---

## AD_LAB Interface Rules

**Goal:** Allow access to Kali, internet (non-private), and default gateway; block all else

1. Navigate to **Firewall > Rules > AD_LAB**.  
2. **Rule 1:** Allow access to Kali VM  
   - **Action:** Pass  
   - **Interface:** AD_LAB  
   - **Address Family:** IPv4  
   - **Protocol:** Any  
   - **Source:** AD_LAB net  
   - **Destination:** Alias = Kali  
   - **Description:** Allow packets to Kali VM  
   - Click **Save**.  
3. **Rule 2:** Allow internet (non-private)  
   - **Action:** Pass  
   - **Interface:** AD_LAB  
   - **Address Family:** IPv4  
   - **Protocol:** Any  
   - **Source:** AD_LAB net  
   - **Destination:** Alias = RFC1918 (Invert match)  
   - **Description:** Allow packets to any non-private address  
   - Click **Save**.  
4. **Rule 3:** Allow access to default gateway  
   - **Action:** Pass  
   - **Interface:** AD_LAB  
   - **Address Family:** IPv4  
   - **Protocol:** Any  
   - **Source:** AD_LAB net  
   - **Destination:** AD_LAB address (gateway)  
   - **Description:** Allow packets to default gateway  
   - Click **Save**.  
5. **Rule 4 (Final):** Block all other traffic  
   - **Action:** Block  
   - **Interface:** AD_LAB  
   - **Address Family:** IPv4 + IPv6  
   - **Protocol:** Any  
   - **Source:** Any  
   - **Destination:** Any  
   - **Description:** Block everything else  
   - Click **Save**, then **Apply Changes**.

---


It should be looking like this
![image](https://github.com/user-attachments/assets/1c3d974f-afe4-4c8e-b15c-3fff8fbd0267)


# FLOATING Rules Desired End State
![image](https://github.com/user-attachments/assets/aa931948-987a-4117-91cf-72a1ba9582ba)


## Grab Kali's New DHCP Reservation
To identify the IP address assigned to your Kali VM via DHCP, open a terminal in Kali and run the following command:

## Reset Kali's Network Interface and Get a New DHCP Lease

To force Kali Linux to request a new IP address via DHCP, you can bring the network interface down and then back up using the following commands:

```
sudo ip link set eth0 down
sudo ip link set eth0 up.
```

after this do 

```
ip a

```

![image](https://github.com/user-attachments/assets/78d03b06-33e2-469b-ae47-720611b8914d)


# Adding Vulnhub VMs to Our VirtualBox Cyber Range

# Mr. Robot

**VM Info on Vulnhub:** [https://www.vulnhub.com/entry/mr-robot-1,151/](https://www.vulnhub.com/entry/mr-robot-1,151/)  
**Vulnhub Download Link:** [https://download.vulnhub.com/mrrobot/mrRobot.ova](https://download.vulnhub.com/mrrobot/mrRobot.ova)

---

## Overview

In this example, we will download a VM from Vulnhub and import it using the `.ova` file format.

### What is an `.OVA` File?

An Open Virtual Appliance (`.ova`) is an open standard file format used to package virtual machines for reuse across different hypervisors. The `.ova` format is directly compatible with VirtualBox, allowing easy import and setup.

When you download the file, your system will usually associate it automatically with VirtualBox.

---

## Import the VM

1. Double-click the `mrRobot.ova` file.  
2. Set the **Name** to `Mr. Robot`.  
3. Configure the **MAC address policy** as needed.  
4. Click **Finish** to import the VM.

---

## Adjust the VM Settings

1. Right-click the `Mr. Robot` VM and select **Settings**.  
2. Add the VM to the **ISOLATED** network.  
3. Click **OK** to save changes.

---

## Start the VM

- Power on the VM. It should receive an IP address from pfSense in the **Isolated LAN**.  
- If your firewall is configured correctly, Kali should be able to route to this LAN.





























