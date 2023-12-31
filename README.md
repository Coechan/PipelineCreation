# PipelineCreation
https://youtu.be/f9D42M9qTQg
Practice
In this practice, we'll build a simple Jenkins pipeline to execute tasks in parallel.

Let’s start by creating a Java application on a GitHub repository that executes de following processes 15 times:

Print the message “Hello, I am <NAME> and I am printing the number <X>”

NAME must be a parameter required to run the application

X is the index of the iteration

Wait a random time (between 1 and 5 seconds) to repeat the process.

If your code is working correctly, the printed text on the console should be the following (assuming “John” is sent as the name parameter):

Hello, I am John and I am printing the number 1

(random time between 1 and 5 seconds passes)

 Hello, I am John and I am printing the number 2

(random time between 1 and 5 seconds passes)

Hello, I am John and I am printing the number 3

(random time between 1 and 5 seconds passes)

Hello, I am John and I am printing the number 4

(repeats until counting to 15)

Now it's time to configure our local Jenkins to have 10 different agents. Once this is completed, we need to create a pipeline with the following characteristics:

The pipeline must have 5 different parameters, which will be the different names on the java application.

The pipeline must execute in parallel, 5 scripts on a different agent each

Each script on their respective agent should clone the newly created repository and its application.

Each script should execute the created application on its respective agent, sending the respective Jenkins name parameter to the application. (The first Jenkins parameter for the first agent script, the second Jenkins parameter for the second agent script, and so on).

After configuring the pipeline, we need to execute it, setting the 5 different name parameters, and check:

5 different agents should be occupied on the executions.

On the pipeline's console, you should see different messages of people counting at different rhythms.

After the 5 agents have counted to 15, the execution should be successfully finished.

Need a hand? Browse the following resources to get unstuck!

Continuous Integration with Jenkins

https://www.jenkins.io/pipeline/getting-started-pipelines/

https://www.jenkins.io/doc/pipeline/tour/hello-world/
