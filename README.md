# IP-quest

# Q1: In the subnet 192.168.0.0/24, what is the highest possible host address?
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

# Q2: In a subnet mask of 255.255.252.0, how many host bits are there?
## Determining the Number of Host Bits in Subnet Mask `255.255.252.0`

## 1. Convert the Subnet Mask to Binary:
The subnet mask `255.255.252.0` in binary is:
- `255` in binary is `11111111`
- `252` in binary is `11111100`
- `0` in binary is `00000000`

So, the subnet mask `255.255.252.0` is:
11111111.11111111.11111100.00000000

## 2. Count the Number of `1` Bits:
Count the number of `1` bits in the subnet mask:
- First octet: `11111111` (8 bits)
- Second octet: `11111111` (8 bits)
- Third octet: `11111100` (6 bits)
- Fourth octet: `00000000` (0 bits)

Total number of `1` bits is: `8 + 8 + 6 + 0 = 22`

## 3. Calculate the Number of Host Bits:
The total number of bits in an IP address is 32. Subtract the number of `1` bits (network bits) from 32 to get the number of host bits:
- Number of host bits = `32 - 22 = 10`

In a subnet mask of `255.255.252.0`, there are **10 host bits**.

# Q3: How many total host addresses are possible with a subnet mask of 255.255.248.0?

## Determining the Total Number of Host Addresses with Subnet Mask `255.255.248.0`

## 1. Convert the Subnet Mask to Binary:
The subnet mask `255.255.248.0` in binary is:
- `255` in binary: `11111111`
- `248` in binary: `11111000`
- `0` in binary: `00000000`

So, the subnet mask `255.255.248.0` is:
11111111.11111111.11111000.00000000


## 2. Count the Number of `1` Bits:
Count the number of `1` bits in the subnet mask:
- First octet: `11111111` (8 bits)
- Second octet: `11111111` (8 bits)
- Third octet: `11111000` (5 bits)
- Fourth octet: `00000000` (0 bits)

Total number of `1` bits is: `8 + 8 + 5 + 0 = 21`

## 3. Calculate the Number of Host Bits:
The total number of bits in an IP address is 32. Subtract the number of `1` bits (network bits) from 32 to get the number of host bits:
- Number of host bits = `32 - 21 = 11`

## 4. Calculate the Total Number of Host Addresses:
The total number of possible host addresses is given by \(2^{\text{number of host bits}}\):
- Number of host addresses = \(2^{11} = 2048\)

## 5. Adjust for Network and Broadcast Addresses:
- Total usable host addresses = \(2048 - 2 = 2046\)

## Conclusion:
With a subnet mask of `255.255.248.0`, there are a total of **2048 possible host addresses**, out of which **2046 are usable** for hosts (excluding the network and broadcast addresses).

# Q4: If a subnet mask is represented in CIDR notation as /21, how many usable IP addresses does the subnet have?

## To determine the number of usable IP addresses in a subnet represented by a `/21` CIDR notation, follow these steps:

### 1. Determine the Number of Host Bits:
In CIDR notation `/21`, the number `21` represents the number of bits used for the network portion of the address. The remaining bits are used for host addresses.

- Total number of bits in an IP address = 32
- Number of host bits = 32 - 21 = 11

### 2. Calculate the Total Number of Host Addresses:
The total number of possible host addresses is given by \(2^{\text{number of host bits}}\):

- Number of host addresses = \(2^{11} = 2048\)

### 3. Adjust for Network and Broadcast Addresses:
In every subnet, two addresses are reserved:
- One for the network address (the first address in the subnet)
- One for the broadcast address (the last address in the subnet)

Thus, the number of usable IP addresses is:

- Usable IP addresses = Total host addresses - 2
- Usable IP addresses = 2048 - 2 = 2046

### Conclusion:
A subnet with a `/21` CIDR notation has **2046 usable IP addresses**.
