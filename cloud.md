# Cloud Services
This section gives pricing for a cloud setup for the company.

[Cloud VM Provider Comparison](#cloud-vm-provider-comparison)  
[Total Cost](#total-cost-of-cloud-vms)  
[Plan](./plan.md)  
[Network Design](./network.md)  
[Security](./security.md)  
[Ethics](./ethics.md)  
[Reflection](./reflection.md)  
[Return to index](./README.md)  


## Work Assignment 
- Trung Hieu HUYNH:
  - Price of "cloud virtual machine" from two real providers
  - Make a table of the specifications, including costs (in Australian dollars) for each.

- Md Mahafuz Faysal: 
  - Do the comparison between Cloud VM and Consumer Desktop PC
  - Discuss the trade-offs.

---


## Cloud VM Provider Comparison

We compared the cost and specifications of a cloud-based virtual machine from **Amazon Web Services (AWS)** and **Microsoft Azure** using their official pricing calculators.

### Specification Requirements
All cloud VMs are intended to replace current Dell PowerEdge tower servers used for a booking system. The following common specification was used for comparison:

| Component                 | Azure Virtual Machine - D4as v5   | AWS Virtual Machine - t3.xlarge  |
|---------------------------|-----------------------------------|----------------------------------|
| **CPU**                   | 4 vCPU                            | 4 vCPU                           |
| **RAM**                 	| 16 GB                             | 16 GB                            |
| **Storage**             	| 500 GB SSD (Premium P20)          | 500 GB SSD (GP3)                 |
| **Operating System**    	| Windows Server                    | Windows Server                   |
| **Region**              	| Australia East (Sydney)           | Asia Pacific (Sydney)            |
| **Monthly Cost**      		| AUD $416                          | AUD $398                         |
| **Annual Cost**       		| AUD $4,992                        | AUD $4779                        |
| **3-Year Total Cost** 		| AUD $14,976                       | AUD $14,338                      |
| **Scalability**       		| High (adjust VM size easily)      | High (adjust VM size easily)     |

### Comparison Table

| Provider | Instance Type        | Specs (vCPU / RAM / Disk) | Monthly Cost (AUD) | 3-Year Cost (AUD) | Export Link |
|----------|----------------------|----------------------------|--------------------|--------------------|-------------|
| AWS      | t3.xlarge            | 4 vCPU / 16GB / 500GB SSD  | $398               | $14,338            | [Download](./images/aws_vm_cost.xlsx) |
| Azure    | D4as v5              | 4 vCPU / 16GB / 500GB SSD  | $416               | $14,976            | [Download](./images/azure_vm_cost.xlsx) |

> Prices are based on the May 2025 estimates from official cloud calculators. Exchange rate: 1 USD = 1.50 AUD (approximate at time of writing).

### Recommendation

We recommend **AWS** for the following reasons:
- Slightly lower 3-year total cost than Azure
- More flexible reserved instance pricing options
- Better integration with third-party tools already used by the company

Both providers meet the technical needs. However, AWS's pricing and long-standing market reputation make it a strong choice for enterprise-grade cloud services.

---

The company currently uses:
- 05 servers at headquarters
- 01 server per branch
- 02 branches

That makes a total of **7 cloud VMs** required.

### Estimated 3-Year Total Cost:

| Provider | Cost Per VM (3 Years) | Number of VMs | Total Cost (AUD) |
|----------|------------------------|----------------|------------------|
| AWS      | $14,338                 | 7              | **$100,366**      |
| Azure    | $14,976                 | 7              | **$104,832**      |

### Summary of Trade-Offs

**Advantages of Cloud VMs:**
- Scalability and flexibility (easy to add more resources)
- No physical maintenance required
- Automatic backups, updates, and monitoring
- High availability and disaster recovery features

**Disadvantages of Cloud VMs:**
- Long-term cost may exceed one-time purchase of physical servers
- Data privacy concerns (data stored offsite)
- Dependence on internet availability
- Learning curve and management overhead

**Conclusion:**  
Given the growth of the company and need for high uptime and remote access, migrating the booking system to **AWS cloud** offers better long-term value, flexibility, and security options.

## Total Cost of Cloud VMs

