# Assignment 1
1. (P6, Page71)
```
a. dprop = m / s
b. dtrans = L / R
c. end-to-end delay = dtrans + dprop
d. The last bit is just leaving Host A.
e. The first bit is in transit and has not yet reached Host B.
f. The first bit has reached Host B
g. See below:
  
  dprop = m / s & dtrans = L / R
  dprop = dtrans
  m / s = L / R
  m = (L / R) * s
  m = (120/(56 x 103))(2.5 x 108)
  m ≈ 536 km
```

2. (P7, Page71)
```
dgen = (56 x 8) / (64 x 103) s
	= 7ms
  
dprop = 10ms
dtrans = (56 x 8) / (2 x 106) s
	= 224µs
  
t = 7ms + 10ms + 224µs
t = 17.224ms
```

3. (P8, Page71)
```
a. #users = (3 x 1000) / 150 = 20 users
b. p = 0.1
c. 120Cn (0.1)n (0.9)120-n
d. ≈ 0.003
```

4. (P10, Page72)
```
trans1 = L/R1
= (1500 x 8) / (2 x 106) s
= 6ms

prop1 = d1 / s1
= (5000 x 103) / (2.5 x 108) s
= 20ms

trans2 = L/R2
= (1500 x 8) / (2 x 106) s
= 6ms

prop2 = d2 / s2
= (4000 x 103) / (2.5 x 108) s
= 16ms

trans3 = L/R3
= (1500 x 8) / (2 x 106) s
= 6ms

prop3 = d3 / s3
= (1000 x 103) / (2.5 x 108) s
= 4ms

dproc = 3ms

End-to-end delay = trans1 + prop1 + dproc + trans2 + prop2 + dproc + trans3
   + prop3
= 64ms
```

5. (P11, Page72)
```
End-to-end delay = trans1 + prop1 + prop2 + prop3
= 46ms
```

6. (P12, Page72)
```
Queuing Delay = [nL + (L - x)] / R
L = 1500b
R = 2 x 106bps
x = 1500 / 2 = 750
n = 4

= 27ms
```

7. (P13, Page72)
```
a.
Queueing Delay of Nth packet = (N - 1)(L / R)
Average Queueing Delay of Nth Packet = (L / R) [(N-1Σi=1i)/N]
= (L / R) [(N(N - 1)) / 2] / N
= (L / RN) [(N(N - 1)) / 2]
= [L (N - 1)] / 2R
= (N - 1) (L / 2R)

b.
Considering a set of packets arrive every LN / R seconds, the queue is empty
every time, so the delay would be the delay of one set, or (N - 1) (L / 2R)
```

8. (P14, Page73)
```
a. IL / R(1-I) + L / R = [IL + L(1 - I)] / R(1 - I) = L / R(1 - L)
b.
```
<img width="597" alt="Screen Shot 2022-06-03 at 8 43 44 PM" src="https://user-images.githubusercontent.com/25465133/171980672-7e3a793f-bd7c-4480-b672-bdc37b54be9b.png">

9. (P15, Page73)
```
Total delay = IL / μ(1 - I) + L / μ
= (L / μ) [1 + I / (1 - I)]
= (L / μ) [1 + (La/μ) / (1 - (La/μ))]
= (L / μ) [1 / (μ - La) / μ]
= (L / μ) [μ / (μ -La)]
= L / (μ - La)
```

10. (P23, Page74)
```
a. Transmission delay = L / Rs
b. Yes, the second link has a low link speed requiring it to wait for the
   transmission to finish. T >= (L / Rc) - (L / Rs)
```

11. (P25, Page75)
```
a. dprog = (2x107)/(2.5x108) = .08s
   R x dprog = 2x106 x .08 = 16x104b
b. The bandwidth delay product is the max bits in the link so 16x104b.
c. The bandwidth delay product is the maximum number of bits that can be in
   transmission.
d. LengthOfBit = s/R = 2.5x108 / 2x106 = 125 meters (Which is longer than a
   football field)
e. BitWidth = sR/m
```

12. (P29, Page75)
```
a. dprog = d/s
   = 3.6x107 / 2.4x108
   = 0.15s
b. R * dprog = 0.15x107 = 15x105
c. xMin = R * 60 = 60x107
```

13. (P31, Page76) (BONUS)
```
a. toSwitch = (8x106)/(2x106) = 4s | toDest = 4 x 3 = 12s
b. toSwitch = (1x104)/(2x106) = 5ms | secondSwitch = 2 x 5 = 10ms
c. toDest = 5 x 3 = 15ms | lastRecieved = 15 + 799x5 = 4.01s | Message
   segmentation has about 1/3 the delay.
d. Small packets may get stuck behind huge queued packets. A bit error could
   cause the whole file to be retransmitted, much larger queues could be needed
   to store the larger packets before retransmission.
e. The destination has to order the packets, there is more network bandwidth
   used because each packet has a separate header so more data flows over the
   network in total.
```

14. (P33, Page77) (BONUS)
```
p1AtDest = 3(S + 80)/R s
T = 3(S + 80)/R + (F/S - 1)[(S + 80)/R] = [(S+80)/R] * (F/S + 2)
dT/dS = 0
(SF + 2S2 - 80F - SF)/RS2 = 0
2s2 - 80F = 0
s2 = 40F
s = 40F1/2
```

15. (Not from textbook)
```
a.
ping n 10 google.com
google.com IP: 142.251.33.7, 11.536ms
cloudflare.com, 104.16.132.229, 27.661ms
oregonstate.edu, 52.27.33.250, 16.346ms
nilsstreedain.com, 104.21.47.133, 13.205ms
Changing the number changes the number of pings sent to the specified server.

b.
```
Hop No. | Source IP Address |	Destination IP Address	|	Round Trip Time (RTT)
-|-|-|-
1 |	10.3.8.52	|	10.3.8.1	|	2.102
2 |	10.3.8.1	|	100.64.0.1	|	3.209
3 |	100.64.0.1	|	* * *	|	* * *
4 |	* * *	|	206.192.244.216	|	4.007
5 |	206.192.244.216	|	72.14.217.83	|	11.462
6 |	72.14.217.83	|	72.14.217.82	|	12.888
7 |	72.14.217.82	|	* * *	|	* * *
8 |	* * *	|	74.125.243.177	|	17.517
9 |	74.125.243.177	|	142.251.55.198	|	10.726
10 |	142.251.55.198	|	74.125.243.177	|	11.787
11 |	74.125.243.177	|	142.251.33.78	|	10.773
12 |	142.251.33.78	|	74.125.243.195	|	13.201
13 |	74.125.243.195	|	142.251.50.245	|	11.127

```
c. The order of responses in Wireshark are the hops in traceroute. The first hop
being to 10.3.8.1, which is my personal router. The second machine is the same
as the table above, 100.64.0.1.
```
