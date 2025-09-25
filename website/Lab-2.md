---
layout: page
title: Lab 2
# permalink: /lab2/
nav_order: 3
---
# 🧑‍💼 AskHR: Automate HR tasks with Agentic AI (Lab 2: Building a simple RAG agent)
    
## Use Case Description


In this lab, we will enable our HR agent in watsonx Orchestrate to answer questions based on a knowledge base. This agent retrieves relevant information from documents to answer user queries.

We will make this agent more powerful with more tools and access to APIs, and enable it to collaborate with other agents in lab3.


## Step by step instructions to build the HR Agent:

1. When you launch watsonx Orchestrate, you'll be directed to this page. Click on the hamburger menu in the top left corner:

    ![image](./imgs/lab-3a/step1.png)

1. Click on the down arrow next to **Build**.  Then click on **Agent Builder**:

    ![image](./imgs/lab-3a/step2.png)

1. Click on **Create agent +**:

    ![image](./imgs/lab-3a/step3.png)

1. Select "Create from scratch", give your agent a unique name (make sure to identify yourself by your initials or name, since this is a shared instance), e.g. "[Your Initial]_HR Agent", and fill in the description as shown below: 

    ```
    You are an agent who handles employee HR queries.  You provide short and crisp responses, keeping the output to 200 words or less. You can answer general questions about company benefits.
    ```  

    Click on **Create**:

    ![image](./imgs/lab-3a/hr_step4.png)

1. We are going to build a knowledge base for the agent. Scroll down the screen to the **Knowledge** section and click on "Choose knowledge".

    ![image](./imgs/lab-3a/hr_step_knowledge.png)

1. Choose "Upload files" and click "Next".

    ![image](./imgs/lab-3a/hr_step_uploadfile.png)

1. Drag and drop the [Employee Benefits.pdf](/f1-week-sg-techxchange/pdfs/Employee-Benefits.pdf) and click on **Next**:

    ![image](./imgs/lab-3a/hr_step6.png)

1. Copy the following description into the **Description** section and click **Save**:

    ```
    This knowledge base addresses the company's employee benefits, including parental leaves, pet policy, flexible work arrangements, and student loan repayment.
    ```

    ![image](./imgs/lab-3a/hr_step_desc.png)

    The knowledge base will take some time to create. After the knowledge base is done, you will be brought back to the Agent Builder UI.

    ![image](./imgs/lab-3a/hr_step_kbase.png)


1. Scroll down to the **Behavior** section. Insert the instructions below into the **Instructions** field:

    ```
    Use your knowledge base to answer general questions about employee benefits. 
    ```

    ![image](./imgs/lab-3a/hr_step12.png)

1. Test your agent in the preview chat on the right side by asking the following questions and validating the responses.  They should look similar to what is shown in the screenshot(s) below:

    ```
    What is the pet policy? 

    ```

    ![image](./imgs/lab-3a/hr_step13.png)

1. Congratulations! You've built your RAG Agent. You can try the following sample questions as well:

    ```
    how many days of leave am i entitled to?

    ```
    ```
    can i work from home 3 times a week?

    ```
    ```
    does the company provide any assistance on loan repayments?

    ```
    ```
    can i update my address?

    ```
    Notice that you get a generic answer when asking to update the address. You will see in the next lab how you can connect it to Employee Address Agent from Lab 1 to actually update the address for you.
