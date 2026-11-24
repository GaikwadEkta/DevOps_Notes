
**1) What is Docker?** 
Docker is an open-source containerization platform used to build, package, deploy and run applications inside lightweight, isolated environments called containers. 
OR 
Docker is an open-source containerization platform used to package an application along with its dependencies, libraries, configuration and runtime environments into a container.


**2) Why we use Docker?**
**Interview answer:**
**"We use Docker to containerize applications. It helps us maintain consistency across development, testing and production environments. It also provides isolation, portability and efficient resource utilization."**

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



**3) What is Containerization?**
Containerization is a process of packaging an application and its dependencies into a lightweight, portable and isolated unit called a container.
How does it work?
1. Developer writes application code.
2. Developer creates a Dockerfile.
3. Docker builds an image using the Dockerfile.
4. Docker runs the image as a container.
5. The container executes the application.
<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/fdf3dd7d-698e-4a18-8473-1dd22d915900" />

