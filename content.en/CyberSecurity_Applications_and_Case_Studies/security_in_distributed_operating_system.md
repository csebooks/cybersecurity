---
title: 'Security in Distributed Operating System: A Comprehensive Study'
weight: 4
---

# SECURITY IN DISTRIBUTED OPERATING SYSTEM: A COMPREHENSIVE STUDY

Sushree Bibhuprada B. Priyadarshini1, Amiya Bhusan Bagjadab2, Brojo Kishore Mishra 3

1 Institute of Technical Education and Research, Bhubaneswar, India. 2 Sambalpur University of Information Technology, Burla, India 3 C. V. Raman College of Engineering, Bhubaneswar, India Email: bimalabibhuprada@gmail.com, amiya7bhusan7@gmail.com, brojokishoremishra@gmail.com

Abstract In recent years, various attacks have been extensively making their passage into the

world of information. In this context, security in Distributed Operating Systems poses it- self as a crucial element. Currently though, whole newer information markets have opened up as playing fields for number of computer criminals, still then it is the job of the user to protect the data. In current chapter, we briefly put light on security policy, security mecha- nism, various categories of attacks, Denial of Service attack, Globus Security Architecture along with distribution of security mechanism. Furthermore, we have also investigated the various strategies of attack that occur frequently in any information system under consid- eration.

Keywords: Access Control, Cryptography, Denial of Service, Distributed Operating System, Fabrication, Threat.

Cybersecurity in Parallel and Distributed Computing. Edited by Dac-Nhuong Le et al. Copyright c© 2018 Scrivener Publishing

 
 
## Introduction to Security and Distributed Systems

The phrase ”Operating system security” is basically the process of ensuring the integrity, confidentiality as well as availability of the operating systems. Fundamentally, Operat- ing system security (abbreviated as: OS security) incorporates the measures involved in protecting the OS from various viruses, worms, threats, malware or external hackers, etc. Basically, a Distributed Operating System is an operating system , which is a software over a gathering of various independent, networked as well as physically distinguished computational nodes. Various jobs are carried out by multiple Central Processing Units (CPUs). Fundamentally, a distributed OS represents an extension of the operating systems employed in networks that assists in higher levels of information interchange and combina- tions of the machines across the network. The logical organization of Distributed systems into various layers is as portrayed in Figure 14.1, where various layers are arranged among one another including kernel and the hardware.

Figure 14.1 Logical organization of distributed systems into various layers

With the popularity of distributed systems, the demand of security is growing day by day with the advent of modern technology in case of Distributed Operating System. However, if the attacker can have the physical contact with the intended machine, then it becomes hectic to protect the concerned system. Moreover, various basic elements of security are as shown in Figure 14.2.

Figure 14.2 Basic Elements of Security  

 
They involve: isolation and minimization of services, access control, cryptography and elimination of vulnerability. Access control represents controlling access to resources present in the system. Likewise, cryptography represents the process of transforming the plain text into cipher text. The text before conversion is known as plain text and after conversion is called cipher text 6.

However, the external threats are the easiest way for protecting. Normally, most of the attacks prevail owing to social engineering, observation, rummaging in the trash, etc. A distributed system represents a network which comprises of various autonomous comput- ers interconnected through a distribution middleware. In this system, sharing of various resources occur. In other words, a distributed system is that system which is designed to assist in the development of various applications as well as services that can makes use of a physical architecture comprising of multiple, processing elements that are autonomous and which do not share primary memory, however, cooperate through transferring asyn- chronous messages over a communication network of interest. The main motto of using distributed systems are: resource sharing, scalability, extensibility, etc. A scenario of in- formation exchange in distributed systems is as shown in Figure 14.3.

Figure 14.3 A scenario of information exchange in distributed systems

As shown in the Figure 14.3, all the systems are interconnected through Local Area Net- work (LAN). A Gateway is present that connects one network to another. In this chapter, we put focus on several mechanisms which are normally integrated in distributed systems for assisting security. Fundamentally, security in distributed systems can be segregated into two parts: the first part is concerned with the communication between users or processes, those dwell on distinct machines. The primitive technique for making sure such secure communication is that of usage of a secure channel.

We will discuss on message confidentiality, message authentication, message integrity in the coming sections. The second part concentrates on authorization that deals with making sure that a process attains access rights to those resources in a distributed system for which it is assigned to. We will discuss on Authorization along with discussion on  

 
access control. Let us first of all discuss the two things to be taken into account while considering the security in any distributed system:

Security Policy: Means what is secure for the system or organization or entity. It basically refers to the constraints on the characteristics of the members and restrictions imposed upon the adversaries by various techniques, viz. Locks, keys, walls, doors, etc.

Security mechanism: A security mechanism is basically designed for preventing or recovering from a security attack. A security service basically uses one or more security mechanisms. Fundamentally, a security service is that which enhances the security of the data processing systems. The following four different types of security threats are commonly present.

- Interception: Refers to the situation where an unauthorized party has the access to data or service. Such situation arises when the communication between two parties is overheard by any other person.

- Interruption: When something is corrupted or lost, the interruption occurs. Ba- sically, it the situation when services or data become unavailable, destroyed, un- usable, etc. In case of denial of service attacks some person tries maliciously for making a service inaccessible to any other party.

- Modification: is concerned with unauthorized change or tampering of data such that it cannot further adhere to its initial specifications. Example: Frequently changing the transmitted data.

- Fabrication: Represents the circumstance where additional data or activity get produced that can not exist normally. For example, an intruder may attempt to append an entry into the password file or the database.

Further, for focussing on security mechanisms through which a policy can be enforced following are some of the mechanisms:

Encryption

Authentication

Authorization

Auditing

Encryption is fundamental to computer security. Encryption transforms data into some- thing an attacker cannot understand. In other words, encryption provides a means to im- plement data confidentiality. In addition, encryption allows us to check whether data have been modified. It thus also provides support for integrity checks. Authentication is used to verify the claimed identity of a user, client, server, host, or other entity. In the case of clients, the basic premise is that before a service starts to perform any work on behalf of a client, it should be learnt 9.

## Relevant Terminologies

The distinct terminologies involved in case of security of DOS are outlined as follows:  

Vulnerability: It indicates a fault in the system that enables an attacking agent to create inappropriate malicious behaviour.

Threat: Threat is some thing that is aimed at threatening the system.

Compromise: It refers to the impact of the vulnerable attack.

Exploit: It means a program exploits the vulnerability/susceptibility.

Payload: Payload means executing the actions pre-planned as the aim of the con- cerned attack.

Root kit: It refers to a set of programs that that hides the presence of the concerned attacker.

Malware: It refers to the generic name for the programs that are malicious.

- Virus: It refers to the program that propagates itself by appending its correspond- ing code to rest of the programs.

- Backdoor: It refers to a secret part of the program, enabling unauthorized access.

- Trojan: It indicates a benign program having an undocumented as well as secret impact on others.

- Logic/time bomb: It refers to a fragment of code that is executed at the time when a particular condition gets satisfied.

- Worm: It refers to the program that propagates itself actively through the corre- sponding network under consideration.

- Bacteria: It refers to the program that can multiply it self for exhausting the sys- tem’s resources locally.

## Types of External Attacks

The various types of external attack that can occur can be shown as illustrated in Figure 14.4.

Figure 14.4 Types of External Attack

Sniffing attack

- This attack is also known as sniffer attack in the context of network security. This attack represents the interception of data by ensnaring the network traffic employing a sniffer.  

 
- The term sniffer refers to an application aimed at capturing the network packets.

- Whenever, the data are transferred across the network, if the packets of the data are not at all encrypted, at that very time a sniffer is employed to read the data packets.

- The attacker can analyse the network and gain the information to eventually cause the concerned network to become corrupted.

- Otherwise, it can read the communications prevailing through the network.

Spoofing

- Spoofing refers to the process of impersonating the machine that is authorized in the information interchange with the victim.

- The frequent spoofing example is IP spoofing. Basically, IP spoofing is a tech- nique that is aimed at gaining access to the machines by which an attacker imper- sonates any other machining by making manipulations on the IP packets.

- It involves modifying the packet header with a forged or spoofed IP address, check sum as well as other values.

Smurfing

- Smurfing is defined as the process of getting access to a secret account that is different from the main document under consideration such that an user can do anything without being detected by any one.

- Smurfing is the phenomenon of impersonating any sort of victim in communica- tion with remaining machines.

Landing

- It is defined as the phenomenon of frauding the victim in communicating with him.

- Various attacks on machines and processes come under such type of attacks.

Information Theft

- This involves the process of taking over the necessary information from various machines.

- There are huge number of information theft affairs found in recent years such as: Credit card Number theft, ATM spoofing, electronic cash theft, database theft, etc.

Denial of Service (DoS)

- Denial of Service (DoS) attack refers to a security event which prevails whenever the attacker initiates actions which prevent the legitimate users from getting access to targeted computers under consideration or any other network resources.

- Typically, such attacks flood the servers, systems or networks with the traffic so as to overwhelm the victim resources for making it hectic or impossible for the authorized users to access it.

The United States Computer Emergency Readiness team (US-CERT) affords various guidelines so as to determine when a DoS attack occurs as follows:  

 
Difficulty in reaching a specific website

Degradation in the performance of the network

Whenever, suspicion arises regarding DoS attack, at that time the organizations or enter- prises contact with their Internet Service Provider (ISP) for checking whether it is owing to DoS attack or due to something else. Afterwards, the ISP assists in mitigating the attack by throttling the malicious traffic employing the load balancers for reducing the impact of at- tacks. Similarly, the feasibility DoS detection can be explored through intrusion prevention systems, intrusion detection systems, etc. Moreover, in Distributed Operating Systems, the network connected devices along with the computer are infected by malware. The various types of DoS attacks are as shown in the Figure 14.5.

Figure 14.5 Types of DoS attacks

## Globus Security Architecture

The idea of security policy and the mode that security mechanisms contribute in distributed systems for enforcement of such type of policies is best established through considering an example. Let us discuss the security policy involved for the Globus wide-area system 3. Basically, Globus is a system that supports large scale distributed computations where many hosts, files, and other resources are concurrently employed for carrying out a compu- tation. These environments are also referred to as computational grids. Further, resources in these grids are many times located in distinct domains of administration which may be positioned in several parts of the world.  

 
The security policy for Globus includes the following statements:

The environment comprises of number of administrative domains.

Local operations: It represents the operations which are conducted only within a sin- gle domain. These are subjected merely to a local domain security policy.

Global operations: This represents the operations concerning several domains that requires the concerned initiator to be known in every domain whereever the operation is being conducted.

Operations between entities in distinct domains need mutual authentication.

Local authentication is replaced by Global authentication.

Controlling access to the resources is mainly subjected merely to local security.

Users can delegate the right to the processes.

Credentials can be shared among processes in the same domain.

Figure 14.6 Globus Security Policy Architecture  

 
It is assumed that the environment comprises of number of administrative domains, such that every domain possesses its policy for local security. It is further taken that local policies cannot be altered since the domain takes partin Globus. Subsequently, security in Globus prohibits itself to operations which can hamper several domains relevant to this issue. Further, Globus assumes that operations which are completely local to a domain are subject only to concerned domain’s security policy. The Globus security policy means that various requests for operations can be initiated either locally or globally. The initiator can be a user or process acting on behalf of a user, must be locally known within each domain.

Once a user or a process acting on behalf of a user get authenticated, it becomes essen- tial to verify the exact access rights with respect to resources. For example, a user wishing to update a file will first have to be authenticated, afterwards, which that can be verified whether concerned user is practically permitted to update the file. The Globus security policy depicts that the access control decisions are framed completely local within the do- main of the location of the accessed resource. Further, Globus focuses on security threats involving multiple domains. Specifically, the security policy demonstrates that the crucial design issues involve the representation of a user in any remote domain, as well as the allo- cation of resources from a remote domain to a user or his representative. The architecture of Global security policy is as shown in the Figure 14.6.

## Distribution of Security Mechanism

Dependencies existing among services concerning trust gives rise to the notion of a Trusted Computing Base (TCB). A TCB represents a set of all security mechanisms in a distributed computer system that are necessary for ensuring a security policy, and which requires to be trusted. The smaller the TCB is, the better one it will be. Further, TCB in a distributed system can incorporate the local operating systems at several hosts. A file server in a dis- tributed file system might need to believe on the several protection mechanisms afforded by corresponding local operating system. Moreover, Middleware-based distributed sys- tems need the trust in the existing local operating systems. If there exists no trust, then part of the functionality of the local operating systems has to be incorporated into the distributed system itself.

## Conclusions

This chapter discusses the various types of attacks that frequently prevail in case of dis- tributed systems by introducing distributed system. Afterwards, we have discussed the concept of policy and mechanism in case of distributed systems. Moreover, we have de- tailed the different types of attacks that prevail in distributed systems including the Denial of Service (DoS) attacks. Thereafter, the concept of Globus Security Architecture as well as the distribution of security mechanism have been confabulated in a nut shell.

**REFERENCES**

1. http://staff.elka.pw.edu.pl/ akozakie/DOS/lecture 10.pdf

2. Thakur, B. S., & Chaudhary, S. (2013). Content sniffing attack detection in client and server side: A survey. International Journal of Advanced Computer Research, 3(2), 7.  

 
3. Khan, S., Gani, A., Wahab, A. W. A., & Singh, P. K. (2018). Feature selection of denial- of-service attacks using entropy and granular computing. Arabian Journal for Science and Engineering, 43(2), 499-508.

4. Sinha, P. K. (1998). Distributed operating systems: concepts and design. PHI Learning Pvt. Ltd.

5. Stallings, W. (2006). Cryptography and Network Security, 4/E. Pearson Education India.

6. Ogiela, M. R., & Ogiela, L. (2018). Cognitive cryptography techniques for intelligent infor- mation management. International Journal of Information Management, 40, 21-27.

7. Firdhous, M. (2012). Implementation of security in distributed systems-a comparative study. arXiv preprint arXiv:1211.2032. https://arxiv.org/ftp/arxiv/papers/1211/1211.2032.pdf

8. https://people.cs.pitt.edu/ mehmud/docs/abliz11-TR-11-178.pdf

9. Tanenbaum, A. S., & Van Steen, M. (2007). Distributed systems: principles and paradigms. Prentice-Hall.
