
**1) What is Docker?**
Docker is an open-source containerization platform used to build, package, deploy and run applications inside lightweight, isolated environments called containers. 
OR 
Docker is an open-source containerization platform used to package an application along with its dependencies, libraries, configuration and runtime environments into a container.

------------------
**Real-world use cases of Docker:**
**1. Microservices architecture -**
Run different application services in separate containers, such as user service, payment service and order service.
**2. CI/CD pipeline -**
Jenkins can build Docker images and deploy containers as part of an automated pipeline.
**3. Cloud deployment -** 
Dockerized applications can be deployed using AWS ECS, EKS and other container platforms.
**4. Development environment -**
Developers can run applications and databases in containers without installing every dependency directly on their laptops.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
**2) Why we use Docker?**
**Interview answer:**
**"We use Docker to containerize applications. It helps us maintain consistency across development, testing and production environments. It also provides isolation, portability and efficient resource utilization."**

-------------------
**Advantages:**
**Portability:** Run the same containerized application across compatible environments.
**Lightweight:** Containers don't need a separate full guest OS.
**Scalability:** Easily create multiple container instances when application demand increases.
**Isolation:** Applications run in separate isolated environments.
**Faster deployment:** Containers can start quickly.
**Consistency:** Reduces environment-related issues.
**Resource efficiency:** Multiple containers can share the host operating system kernel.

Suppose we develop a Python application on our laptop.

Our application works perfectly, but when we deploy it on another server, it fails because:
- Python versions are different.
- Required libraries are missing.
- Dependencies are incompatible.
- Environment configurations are different.
This is a common problem in software development.

Docker solves this problem by packaging the application and its dependencies into a container.

समजा आपण आपल्या laptop वर application तयार केले आणि ते व्यवस्थित चालत आहे. पण तेच application दुसऱ्या server वर deploy केल्यावर dependencies किंवा versions वेगळे असल्यामुळे चालत नाही.
Docker application सोबत लागणाऱ्या dependencies आणि configurations एका container मध्ये package करतो.
त्यामुळे वेगवेगळ्या environments मध्ये application चालवणे सोपे होते.

**"Docker helps developers and DevOps engineers build, package and deploy applications consistently across different environments."**
<img width="1717" height="867" alt="image" src="https://github.com/user-attachments/assets/7ba8a028-a65e-4693-9122-585d38930205" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

**3) What is Containerization?**
Containerization is a process of packaging an application and its dependencies into a lightweight, portable and isolated unit called a container.

How does it work?
1. Developer writes application code.
2. Developer creates a Dockerfile.
3. Docker builds an image using the Dockerfile.
4. Docker runs the image as a container.
5. The container executes the application.
<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/fdf3dd7d-698e-4a18-8473-1dd22d915900" />

----------------------
**Important terms:
Dockerfile -->	Instructions to build an image
Docker Image -->	Read-only template used to create containers
Docker Container -->	Running instance of an image**

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

**4) Container vs Virtual Machine (VM)**
Suppose we have one physical server.
Using virtualization, we can create three VMs, each having its own operating system.
Using Docker, we can run multiple containers on the same host OS without installing a separate full operating system for every container.

"The **main difference** is that virtual machines require a separate guest operating system, whereas Docker containers share the host operating system kernel. That's why containers are generally lightweight and start faster than virtual machines."

**Virtual Machine architecture:**
- Physical hardware
- Host operating system
- Hypervisor
- Multiple virtual machines
- Each VM has its own guest OS, libraries and application.
**Docker container architecture:**
- Physical hardware
- Host operating system
- Docker Engine
- Multiple containers
- Containers share the host OS kernel while maintaining process and resource isolation.

<img width="1491" height="858" alt="image" src="https://github.com/user-attachments/assets/09c107c7-fbd1-4a98-9144-8e68dcc947c0" />


-------------------------------------------------------------------------------------------------------------------------------------------------------------------

**5) Can Docker containers run different operating systems?**
"Containers share the host kernel, so they cannot independently run a completely different kernel. For example, Linux containers require a Linux kernel. On Windows and macOS, Docker Desktop uses a Linux virtual machine to run Linux containers."

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

**6) Are Docker containers completely isolated?**
"No. Docker containers provide process and resource isolation using Linux kernel features such as namespaces and cgroups, but they share the host kernel. They are not equivalent to full virtual machines in terms of isolation."

------------------------------------------------------------------------------------------------------------------------------------------------------------------

**7) Disadvantages / Limitations of Docker**
1. Shared kernel: Containers share the host kernel, so they don't provide the same isolation boundary as VMs.
2. Persistent storage management: Container writable data can be lost when a container is removed unless appropriate storage is configured.
3. Networking complexity: Managing communication between multiple containers can become complicated.
4. Monitoring: Large container environments require proper monitoring and logging.
5. Security risks: Misconfigured containers, excessive privileges and vulnerable images can create security risks.
6. Management complexity: Large-scale container deployments need orchestration tools like Kubernetes.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------

**8) What is the difference between Docker and Containerization?**
"Containerization is a technology or process of packaging applications with their dependencies into containers. Docker is a platform that helps us implement containerization."

----------------------------------------------------------------------------------------------------------------------------------------------------------------
**9) What happens when a Docker container is deleted?**
"When we delete a container, its writable layer and data stored only inside that layer are removed. However, the Docker image and separately stored volume data remain unless we explicitly remove them."

----------------------------------------------------------------------------------------------------------------------------------------------------------------
**10) Can we run multiple containers on a single machine?**
"Yes, we can run multiple containers on a single machine. Docker provides isolation between containers, and they can share the host operating system kernel."

---------------------------------------------------------------------------------------------------------------------------------------------------------------
**11) Is Docker a replacement for Virtual Machines?**
"No. Docker and virtual machines solve different problems. Containers are lightweight and share the host kernel, whereas virtual machines provide separate guest operating systems. Both technologies can be used together."

----------------------------------------------------------------------------------------------------------------------------------------------------------------

**12) Docker Image vs Docker Container**
A **Docker Image** is a read-only template used to create Docker containers. It contains the application code, runtime, libraries, dependencies and configuration required to run an application.
**Example:**
Suppose we want to run an Nginx web server.
First, we download the Nginx Docker image from Docker Hub. This image contains everything required to run Nginx.

A **Docker Container** is an instance of a Docker image. It provides an isolated environment in which an application runs.
container is created from a Docker image and is used to run the application.
**For example:**
- Nginx image → Nginx container
- MySQL image → MySQL container
- Ubuntu image → Ubuntu container

-----------------------------------------------------------------------------------------------------------------------------------------------------------------
