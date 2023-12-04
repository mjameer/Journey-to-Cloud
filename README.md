### Jorney-to-Cloud

In the fast-evolving landscape of technology, organizations are constantly challenged to modernize their legacy applications and embrace cloud-native architectures. This blog narrates the journey of transforming multiple Java applications, initially deployed in the cloud, through various stages of evolution – from Mavenization to migration to Liberty, containerization, and finally deployment in Azure Kubernetes Service (AKS). While reflecting on the accomplishments, the narrative also highlights key learnings and pivotal decisions made throughout the process.


This particular GIF summarizes how our work was for the last 6 months. I can call it a day and say the blog is done because this is really what you'll be doing as well if you're planning to move into containers, and eventually into Kubernetes

![PbB](https://github.com/mjameer/Jorney-to-Cloud/assets/11364104/ca3c7e1b-a0ae-4048-82b7-541425ff319f)

Following are the phases we went through during our cloud migration strategy 

### The Mavenization Phase:

The journey began with the Mavenization of existing applications, a crucial step towards standardizing project structures and dependencies. This initiative aimed to streamline the build process, enhance project maintainability, and pave the way for subsequent cloud-based transformations.

### Migration to Liberty:

Following Mavenization, the team migrated applications to Liberty, an open-source runtime for building, deploying, and managing Java applications. Liberty's lightweight nature and support for microservices architecture made it an ideal choice for the evolving landscape.

### Containerization Project - Dockerization:

The next step for our team was to embark on a significant project - Dockerization. Docker containers provide a standardized unit for packaging and shipping applications, ensuring consistency across different environments. This initiative required meticulous evaluation and adoption of Docker within the existing infrastructure, a process that involved both technical challenges and gaining developer buy-in.

### Container Orchestration via Kubernetes

With Docker containers in place, the focus shifted to container orchestration. The team recognized the need for a robust orchestration system to manage containers efficiently. Kubernetes emerged as the chosen technology, providing scalability, integration capabilities, and a thriving community.

### Externalize configurations

With the introduction of k8s, the app team was able to externalize the app configurations, which provided us with a more secure mechanism to store and retrieve credentials and other critical data

![ezgif com-crop](https://github.com/mjameer/Jorney-to-Cloud/assets/11364104/4ad37867-c4fc-4cd5-88ec-de47a5b7cb14)

### Database Migration Motivation:
In this cloud journey process, we migrated some of the applications DB from MsSQL to Progress as Postgres provided no license cost when compared to MsSQL which costs about 800/per month. This cost-effective move presented an opportunity to optimize resources and allocate budgets more efficiently.

### Unforeseen Challenges:

However, the migration introduced an unexpected challenge. The applications, originally designed for intranet accessibility, now had to traverse the network between the intranet and Azure's internet. This inter-network communication led to noticeable latency issues, impacting the performance of the applications. Recognizing the need for a swift resolution, the team proactively sought solutions to mitigate this newfound challenge.

### Introduction of Internal Openshift:

To address the performance issues arising from the network latency, the team pivoted to an internal Openshift solution. Openshift, with its container orchestration capabilities, became a strategic choice for applications requiring extensive on-premises and off-premises connections. This shift aimed to streamline and optimize the network path, providing a more efficient and responsive experience for users.


### Adapting Midway:

The decision to adopt Internal Openshift was not part of the initial plan but arose as a pragmatic response to unforeseen challenges. Midway through the migration process, the team demonstrated flexibility and adaptability, prioritizing the user experience and overall application performance.

### Balancing Cost and Performance:

This experience highlights the delicate balance organizations must strike between cost considerations and performance optimization during complex migrations. While cost-effective solutions like Postgres can be advantageous, addressing the subsequent challenges in network performance becomes equally crucial to ensure a seamless user experience.

### Conclusion 

In conclusion, the legacy applications' journey to the cloud showcases a meticulous process of modernization, from Mavenization to Dockerization, and finally, the adoption of Kubernetes for container orchestration.

Looking back, one thing I wish that we could have done differently once we saw how it happened end to end is we should have done early on the evaluation phase with proper POCs and the results of that. So the decision-making would have been even clearer and better. That took some time for us, so that is something I would consider in any of such next phases of migration. 

### The End

![image](https://github.com/mjameer/Jorney-to-Cloud/assets/11364104/c2c187dc-0908-4135-b84c-930971048114)



