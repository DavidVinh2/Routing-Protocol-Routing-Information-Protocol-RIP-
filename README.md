# Routing Protocol Project-Routing Information Protocol(RIP)

# Overview

Routing Information Protocol (RIP) was created to allow dynamic routing for small networks. It does not understand Variable Length Subnet Mask (VLSM) because RIP exists this facility. RIP version 2 addresses this shortcoming by recognizing VLSM.

# Lab Requirements

This repository provides a full configuration solution for the following tasks:
1. Set up all physical cables and connections.
2. Initialize routers.
3. Configure interface IP addresses.
4. Configure routing protocol
5. Verify that router can ping any other router.
6. Check routing tables.

# Topology

<img width="1684" height="762" alt="image" src="https://github.com/user-attachments/assets/5e00f92d-2932-445f-aa43-5cedeeb4295d" />

# Lab Walkthrough

1. After connecting two routers together using a crossover cable, I added IP addresses to the routers connecting the interfaces and then the loopback interfaces.

<img width="1362" height="544" alt="Connection of R0" src="https://github.com/user-attachments/assets/180f6dd3-64c2-4d5e-911c-d4ad61c0d168" />
<img width="1370" height="590" alt="Connection of R1" src="https://github.com/user-attachments/assets/f2517277-a3b0-49b9-8d05-94842fb10795" />

2. I pinged from R0 to R1 to check the connection works.

<img width="1352" height="184" alt="Screenshot of ping 192" src="https://github.com/user-attachments/assets/28e3dd05-3f03-4cd1-91ed-0e7069b20a6f" />

3. I configured RIP on both R0 and R1 to advertise the connected networks.

<img width="1224" height="190" alt="Screenshot of configure router RIP for R0" src="https://github.com/user-attachments/assets/2230cad2-51fa-45c4-8fe2-a9467157a583" />

<img width="1364" height="174" alt="Screenshot of router configure RIP for R1" src="https://github.com/user-attachments/assets/f25658ae-ef24-49f8-8b64-a90b207238d4" />


4. I checked the routing table with "show ip route" command and routing configurations with "show ip protocols" command.

<img width="1256" height="758" alt="Screenshot 2026-09-22 153237" src="https://github.com/user-attachments/assets/7d1ce17d-779a-493b-88fa-f6f8926bd260" />

<img width="1332" height="562" alt="Screenshot 2026-09-22 153356" src="https://github.com/user-attachments/assets/43d5721c-c5e9-433e-9dc3-2e4436e805e0" />


5. I pinged the network address.

<img width="1346" height="174" alt="Screenshot 2026-09-22 153746" src="https://github.com/user-attachments/assets/500165b3-d140-424d-a250-4cc6f9e589f3" />

6. I changed the version of RIP to 2 and checked the routing table again. I would need to clear it first with "clear ip route" command.

<img width="2434" height="822" alt="image" src="https://github.com/user-attachments/assets/cb640600-b3d3-4cb9-9002-1b81eb87ef8f" />
<img width="964" height="424" alt="image" src="https://github.com/user-attachments/assets/65216ea3-b424-4d45-9a79-960aa87021c9" />

# Conclusion

Both routers had an administrative distance of 120 with a metric of 1. The metric of 1 is better than 2. Metric values are assigned by routing protocol. 


