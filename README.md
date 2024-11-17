# CMPE-72-Jenkins

Here's a comprehensive README file for your assignment:

---

# **Jenkins Integration and GitHub Project Management**

## **Overview**  
This project demonstrates the integration of Jenkins with a GitHub repository, setting up a build trigger, and managing tasks with GitHub Projects. The assignment is divided into three parts:  
1. Integrating Jenkins with a GitHub repository.  
2. Implementing a build trigger using GitHub Webhooks.  
3. Setting up and managing a GitHub Project with tasks and automation.

---

## **Table of Contents**  
1. [Prerequisites](#prerequisites)  
2. [Part A: Jenkins Integration with GitHub Repository](#part-a-jenkins-integration-with-github-repository)  
   - Installation  
   - GitHub Repository Integration  
3. [Part B: Implementing a Build Trigger](#part-b-implementing-a-build-trigger)  
   - Webhook Setup  
   - Testing the Trigger  
4. [Part C: GitHub Project Quickstart](#part-c-github-project-quickstart)  
   - Project Setup  
   - Task Management and Automation  
5. [Screenshots and Outputs](#screenshots-and-outputs)  
6. [Conclusion](#conclusion)

---

## **Prerequisites**  
Before starting, ensure you have:  
- A GitHub account and repository.  
- Jenkins installed on your machine ([Installation guide for macOS](https://www.jenkins.io/doc/book/installing/macos/) | [Windows](https://www.jenkins.io/doc/book/installing/windows/)).  
- Git Plugin installed in Jenkins ([Git Plugin documentation](https://plugins.jenkins.io/git/)).  
- Admin access to configure GitHub Webhooks.  

---

## **Part A: Jenkins Integration with GitHub Repository**

### **1. Install Jenkins**  
- Follow the [Jenkins installation guide](https://www.jenkins.io/doc/book/installing/) for your operating system.  
- Start Jenkins and set up an admin account.  

### **2. Configure Git Plugin**  
- Navigate to `Manage Jenkins` > `Manage Plugins`.  
- Install the `Git Plugin`.  

### **3. Set Up Your GitHub Repository**  
- Create a new Jenkins project (`New Item` > `Freestyle Project`).  
- Under `Source Code Management`, select `Git` and enter your GitHub repository URL.  
- Add credentials if required.  

---

## **Part B: Implementing a Build Trigger**

### **1. Webhook Setup**  
- Go to your GitHub repository settings > `Webhooks`.  
- Add a new webhook with the URL: `http://<Jenkins_URL>:<port>/github-webhook/`.  
- Choose `application/json` and select the desired events (e.g., `push`).  

### **2. Configure Jenkins Build Trigger**  
- In your Jenkins project configuration, under `Build Triggers`, select `GitHub hook trigger for GITScm polling`.  

### **3. Test the Webhook**  
- Push a commit to your GitHub repository.  
- Verify that Jenkins triggers a build automatically.

---

## **Part C: GitHub Project Quickstart**

### **1. Introduction**  
The GitHub Project feature helps in task organization and progress tracking.  

### **2. Creating a Project**  
- Go to your repository > `Projects` > `+ New Project`.  
- Select a template or create a custom project.  

### **3. Setting Project Description and README**  
- Add a description to your project.  
- Commit a `README.md` file to your repository.  

### **4. Task Management**  
- Add issues to your project by linking them from your repository or creating new ones.  
- Add draft issues for unfinalized tasks.  

### **5. Adding Fields and Views**  
- Create custom fields for `Priority` and `Iteration`.  
- Group issues by `Priority` and save this view.  

### **6. Board Layout and Automation**  
- Change the project layout to `Board` and define columns like `To Do`, `In Progress`, and `Done`.  
- Configure automation to update issue status based on branch creation or pull request merges.


## **Screenshots and Outputs**  
- Include screenshots of:  
  1. Jenkins project configuration with the GitHub repository URL.  
  2. Webhook setup in GitHub.  
  3. A successful Jenkins build triggered by a GitHub commit.  
  4. GitHub Project setup with tasks, fields, and automation enabled.

---

## **Conclusion**  
This project showcases a seamless CI/CD pipeline using Jenkins and effective task management with GitHub Projects. By integrating these tools, developers can automate builds, improve productivity, and enhance collaboration.
