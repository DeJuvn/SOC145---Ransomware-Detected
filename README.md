<h1>SOC145 - Ransomware Detected</h1>


<h2>Monitoring</h2>

- <b>Details:</b>
<br />

![image](https://user-images.githubusercontent.com/131769679/235164879-e4299b09-cfd2-4872-84c7-5ad0d9609da7.png)


<h2>Analyzing Content</h2>

- <b>We download the zip file and extract the content. We can then create hashes for the zip files. Hashes are extremely useful to identify a piece of malware.</b> 

![image](https://user-images.githubusercontent.com/131769679/235165206-41357dc6-4414-49e7-a56d-07d6c39499fa.png)


<h2>Virus Total</h2>

- <b>Now we can search the hash on Virus Total. We can use this to search through their data to identify files that the hash provided.</b>

![image](https://user-images.githubusercontent.com/131769679/235165336-e676a07a-37c0-4e85-8ccb-b470d7055329.png)

Now we can see that according to Virus Total the file hash we provided is malicious.

<h2>Hybrid Analysis</h2>

- <b>Using Hybrid Analysis we see more results proving the executable is malicious. "ab.bin"</b>

![image](https://user-images.githubusercontent.com/131769679/235165914-89d0a0fc-5730-4a7d-965d-0f6ee83bea20.png)

![image](https://user-images.githubusercontent.com/131769679/235165969-9efe2618-8231-4d1d-974a-ab98a0e0b099.png)

- <b>"ab.exe"</b>

![image](https://user-images.githubusercontent.com/131769679/235166053-695726f4-bdd3-46b6-ba06-251b57280c99.png)

![image](https://user-images.githubusercontent.com/131769679/235166420-199d4ef5-f1fa-4666-a84e-58a682bbd84d.png)


<h2>Indicators of Compromise (IOC)</h2>

- <b>We have found several strings in the "ab.bin" and "ab.exe" files.</b>

![image](https://user-images.githubusercontent.com/131769679/235166591-9b73be58-59e6-4319-ba2e-baba2a3572c3.png)

![image](https://user-images.githubusercontent.com/131769679/235166638-935cfe05-0107-482e-958c-47142b43ff71.png)

- <b>avaddonbotrxmuyl(dot)onion</b>
- <b>0b486fe0503524cfe4726a4022fa6a68</b>
- <b>Sha256: 1228d0f04f0ba82569fc1c0609f9fd6c377a91b9ea44c1e7f9f84b2b90552da2</b>

<h2>Checking The Logs</h2>

- <b>We are going to use the logs to check the IPs of the target reached out to.</b>

![image](https://user-images.githubusercontent.com/131769679/235167290-c0ce86c1-16c9-46cb-8fc1-8988bf87198c.png)

![image](https://user-images.githubusercontent.com/131769679/235167321-a30673f8-2e05-4685-bb40-124c005ced55.png)

![image](https://user-images.githubusercontent.com/131769679/235167368-fa83b2a1-a892-4c3f-b847-cb420e1be515.png)

- <b>No ransomware indications.</b>

<h2>Endpoint Security</h2>

![image](https://user-images.githubusercontent.com/131769679/235167644-bc6c8bb7-f5c8-4eed-bde2-8980fe79378a.png)

- <b>Here we can check the process history.</b>

![image](https://user-images.githubusercontent.com/131769679/235167762-b6dad7d2-4b53-4d9b-8344-06c216602114.png)

- <b>Confirmed that the "ab.exe" file has been executed.</b>

![image](https://user-images.githubusercontent.com/131769679/235167922-47effb2b-de74-4749-b775-075347339f5a.png)

![image](https://user-images.githubusercontent.com/131769679/235167965-55e439bf-7871-44f7-89ee-fb814643f718.png)

- <b>The target has been contained</b>

![image](https://user-images.githubusercontent.com/131769679/235168085-b189d959-b0b2-463d-89da-ee8c83c3ba7b.png)

<h2>Case Management</h2>

- <b>Define Threat Indicator: other</b>
- <b>Check if the malware is quarantined/cleaned: Not Quarantined</b>
- <b>Analyze malware in 3rd party tools and find C2 address: Malicious</b>
- <b>Check If Someone Requested the C2: Not Accessed</b>
- <b>Add Artifacts:</b>

![image](https://user-images.githubusercontent.com/131769679/235168480-04895782-0033-4a72-8aab-2c9c46752fac.png)

- <b>Analyst Note:</b>

![image](https://user-images.githubusercontent.com/131769679/235168600-062f6774-b035-4cd6-b8cf-780752a881d7.png)

- <b>Finish Playbook:</b>

![image](https://user-images.githubusercontent.com/131769679/235168766-05c639d8-ba14-4300-a0c1-e0a2cdb8f6c5.png)

- <b>Case Closed:</b>

![image](https://user-images.githubusercontent.com/131769679/235168890-6af0a91b-e270-4d3d-9894-f19f906dbca7.png)


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
