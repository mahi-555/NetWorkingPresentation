TCP Congestion and Slow Start Algorithm
Presentation Overview
This repository contains an academic presentation about TCP Congestion
Control and the Slow Start Algorithm. It explains how Transmission
Control Protocol (TCP) adjusts its sending rate to use network capacity
efficiently while reducing the risk of congestion.

Prepared by Monira Akter Mahin (ID: IT24017), Department of
Information and Communication Technology (ICT), Mawlana Bhashani Science
and Technology University (MBSTU), Bangladesh.
Objectives
- Explain network congestion and its effects on communication.
- Describe the TCP congestion window (cwnd) and slow start threshold
  (ssthresh).
- Explain Slow Start and Congestion Avoidance.
- Introduce Additive Increase and Multiplicative Decrease (AIMD).
- Describe Fast Retransmit and Fast Recovery.
- Compare the congestion responses of TCP Tahoe, TCP Reno, and CUBIC.
Presentation Contents
1. Introduction and research problem
2. Background: What is network congestion?
3. Related work and research gap
4. Methodology
5. Slow Start algorithm
6. Congestion window growth during Slow Start
7. Congestion Avoidance and AIMD
8. Fast Retransmit and Fast Recovery
9. Experimental setup
10. Results and discussion
11. Quantitative comparison
12. Conclusions and future work
13. Selected references
Key Concepts
Congestion Window (cwnd)
The congestion window controls how much unacknowledged data a TCP sender
may have in the network. TCP adjusts this window according to network
feedback.
Slow Start
Slow Start begins with a small congestion window. In the idealised
example in the presentation, the window doubles during each round-trip
time (RTT): 1, 2, 4, 8, and 16 segments. TCP leaves Slow Start when the
threshold is reached or congestion is detected.
Slow Start Threshold (ssthresh)
The threshold determines when TCP changes from exponential growth in
Slow Start to the more gradual growth of Congestion Avoidance.
Congestion Avoidance and AIMD
During Congestion Avoidance, the congestion window increases by
approximately one segment per RTT. When loss is detected, TCP reduces
the window. This behaviour is described as Additive Increase and
Multiplicative Decrease (AIMD).
Fast Retransmit and Fast Recovery
When the sender receives three duplicate acknowledgements, it can
retransmit the missing segment without waiting for the retransmission
timeout. TCP Reno then uses Fast Recovery. A timeout is treated as a
stronger congestion signal and causes the congestion window to restart
from one segment in the simplified model used in the presentation.
Methodology and Scope
The presentation uses an idealised, textbook RTT-round model of a
single TCP flow over one bottleneck link. It compares TCP Tahoe and TCP
Reno under the same threshold and loss event.

The illustrated evaluation measures are:
- Congestion window size (cwnd) in segments per RTT
- Recovery behaviour after packet loss
Important: The graphs and numerical examples are illustrative model
results, not measurements collected from a live network or a dataset.
The presentation suggests that the behaviour could be reproduced or
investigated further using ns-3 or Wireshark.
Main Discussion
The presentation highlights that TCP Reno can recover more quickly than
TCP Tahoe after three duplicate ACKs because Reno uses Fast Recovery
instead of restarting the congestion window from one segment. In the
simplified comparison, both algorithms restart from one segment after a
timeout.
Tools and Technologies Mentioned
- TCP: Transmission Control Protocol
- RTT: Round-Trip Time
- Wireshark: Network protocol analyser suggested for further
  practical observation
- ns-3: Network simulator suggested for future experiments
No software implementation or live network experiment is included in the
presentation itself.
Future Work
- Simulate TCP flows using ns-3.
- Capture and analyse TCP traffic using Wireshark.
- Compare Reno, CUBIC, and BBR under different network conditions.
- Study the effects of delay, packet loss, buffer size, and competing
  traffic.
References
1. V. Jacobson, "Congestion Avoidance and Control," ACM SIGCOMM, 1988.
2. M. Allman, V. Paxson, and E. Blanton, "TCP Congestion Control," RFC
   5681, IETF, 2009.
3. L. Xu, S. Ha, I. Rhee, V. Goel, and L. Eggert, "CUBIC for Fast and
   Long-Distance Networks," RFC 9438, IETF, 2023.
4. N. Cardwell et al., "BBR: Congestion-Based Congestion Control,"
   Communications of the ACM, 2017.
Presenter
Monira Akter Mahin
ID: IT24017
Department of Information and Communication Technology (ICT)
Mawlana Bhashani Science and Technology University
Session: 2023--24
Santosh, Tangail, Bangladesh
