# Task 8 [Day 2] Log analysis: O Data, All Ye Faithful
# The Story
![Image](https://tryhackme-images.s3.amazonaws.com/user-uploads/5de96d9ca744773ea7ef8c00/room-content/157a546b4478b174643dabf30604e114.svg)

## *Answer Of The Question Below*

#### How many packets were captured (looking at the PacketNumber)?
![Image](1.png)
###### df.count()
![Image](1(2).png)
```python
100
```
#### What IP address sent the most amount of traffic during the packet capture?
![Image](2.png)
###### df.groupby(['Source']).size()
![Image](2(2).png)
```python
10.10.1.4
```
#### What was the most frequent protocol?
![Image](3.png)
###### df.groupby(['Protocol']).size()
![Image](3(2).png)
```python
ICMP
```
