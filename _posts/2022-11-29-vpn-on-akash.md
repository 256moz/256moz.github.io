---
layout: page
title: "VPN on Akash Network"
permalink: /vpn-on-akash
categories: AKASH VPN
---

Assuming you:

* have [reasons](https://decrypt.co/115486/infura-collect-metamask-users-ip-ethereum-addresses-after-privacy-policy-update) why you'd like a VPN
* installed [Cloudmos Cloud Deploy for Akash](https://cloudmos.io/cloud-deploy)
* funded your Cloudmos wallet with [acquired Akash $AKT tokens](https://akash.network/token)

Here's how to spin up a VPN:

1. Select `Templates` and search for `VPN`

	![Search for VPN](/assets/1_akash_vpn/1_cloudmos_softether_template.png)

2. Click `Deploy`

	![Select Deploy](/assets/1_akash_vpn/2_select_deploy.png)

3. Click `Create Deployment`

	![Create Deployment](/assets/1_akash_vpn/3_create_deployment.png)

4. Confirm 5 AKT deposit

	![Click Deposit](/assets/1_akash_vpn/4_click_deposit.png)

5. Approve the Deployment Transaction

	![Approve Deploy TX](/assets/1_akash_vpn/5_txdeploy.png)

6. Select a Provider Bid and Accept
	
	![Approve Deploy TX](/assets/1_akash_vpn/6_acceptbid.png)

7. Approve Lease Transaction

	![Approve Lease TX](/assets/1_akash_vpn/7_txlease.png)

8. Under `Leases`, take note of forwarded port

	![Note URL and port](/assets/1_akash_vpn/8_urlport.png)

9. Under `Logs`, copy text in GREEN box, replacing (A) and (B) from `Step 8`. Note Username and Password for OpenVPN later.

	![Create OVPN file](/assets/1_akash_vpn/9_ovpnfile.png)

10. Under Network Settings in Ubuntu, click `+` to add a new VPN

	If you do not see this, these might help:

	```
	sudo apt-get -y install network-manager-openvpn
	sudo service network-manager restart
	```

	![Network Settings VPN](/assets/1_akash_vpn/10_netsettings.png)

11. Import from file

	![Import OVPN file](/assets/1_akash_vpn/11_importovpn.png)

12. Enter Username/Password from `Step 9`

	![User Pass from Step 9](/assets/1_akash_vpn/12_userpass.png)

13. Save settings
	
	![Save](/assets/1_akash_vpn/13_savesettings.png)

14. Toggle VPN on

	![Toggle VPN on](/assets/1_akash_vpn/14_toggleon.png)

If you're using MacOS, you should be able to use the OVPN file import and credentials with the [MacOS OpenVPN client](https://openvpn.net/client-connect-vpn-for-mac-os/).