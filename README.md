# IP-quest

# Q: In the subnet 192.168.0.0/24, what is the highest possible host address?
## Highest Possible Host Address in Subnet `192.168.0.0/24`

## Breakdown of the Subnet:
- The `/24` notation indicates a **subnet mask** of `255.255.255.0`, meaning the first 24 bits represent the **network portion**, and the last 8 bits are reserved for **host addresses**.

- The range of host addresses starts after the network address and ends before the broadcast address.

## Calculating the Host Range:
- **Network Address**: `192.168.0.0` (This is reserved as the network identifier, so it cannot be assigned to a host.)
- **Broadcast Address**: `192.168.0.255` (This is reserved for sending broadcast messages to all hosts on the network.)

## Highest Host Address:
- The highest possible host address is the one just before the broadcast address:  
  **192.168.0.254**.

## Conclusion:
The highest possible host address in the subnet `192.168.0.0/24` is **192.168.0.254**.
```
