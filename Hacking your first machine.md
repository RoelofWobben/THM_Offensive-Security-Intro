# Your First Hack

We will use a command-line application called "Gobuster" to brute-force FakeBank's website to find hidden directories and pages. Gobuster will take a list of potential page or directory names and try accessing a website with each of them; if the page exists, it tells you.

**Step 1. Open A Terminal**

A terminal, also known as the command line, allows us to interact with a computer without using a graphical user interface. On the machine, open the terminal by clicking on the Terminal icon on the right of the screen.

![terminal](images/terminal.png)

**Step 2. Use Gobuster To Find Hidden Website Pages**

Most companies have an admin portal page, giving their staff access to basic admin controls for day-to-day operations. For a bank, an employee might need to transfer money to and from client accounts. Due to human error or negligence, there may be instances when these pages are not made private, allowing attackers to find hidden pages that show or give access to admin controls or sensitive data.

To begin, type the following command into the terminal to find potentially hidden pages on FakeBank's website using Gobuster (a command-line security application).

```
gobuster -u http://fakebank.thm -w wordlist.txt dir
```

![gobuster](images/gobuster.png)

In the command above, '-u' is used to state the website we're scanning, -'w' takes a list of words to iterate through to find hidden pages.

You will see that Gobuster scans the website with each word in the list, finding pages that exist on the site. Gobuster will have told you the pages in the list of page/directory names (indicated by Status: 200).

![gobuster_output](images/gobuster2.png)

From this page, an attacker has authorized access and can steal money from any bank account. 

![bank](images/fakebank.png) 

As an ethical hacker, you would (with permission) find vulnerabilities in their application and report them to the bank to fix them before a hacker exploits them.

Your mission is to transfer $2000 from bank account 2276 to your account (account number 8881). If your transfer was successful, you should now be able to see your new balance reflected on your account page.

Go there now and confirm you got the money! (You may need to hit Refresh for the changes to appear)

# Solution 

![bank_transfer](images/bank_transfer.png)

![bank_transfer_success](images/bank_transfer_success.png) 

![bank_hacked](images/bank_hacked.png)








