<h1>Module 1 Homework</h1>

<h2>Docker & SQL
In this homework we'll prepare the environment and practice with Docker and SQL</h2>

<h3>Question 1. Knowing docker tags</h3>

Run the command to get information on Docker

<code>docker --help</code>

Now run the command to get help on the "docker build" command:

<code>docker build --help</code>

Do the same for "docker run".

Which tag has the following text? - Automatically remove the container when it exits

- <code>--rm</code>

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/7e959f36-6b34-4860-839c-15f122242f0f)


<h3>Question 2. Knowing docker tags</h3>

Run docker with the python:3.9 image in an interactive mode and the entrypoint of bash.
Now check the python modules that are installed ( use ```pip list``` ). 

What is version of the package *wheel* ?

- 0.42.0

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/1b3ab401-82f0-4113-9623-baa2cfe004b6)


<h3>Question 3. Count records</h3>

How many taxi trips were totally made on September 18th 2019?

Tip: started and finished on 2019-09-18. 

Remember that `lpep_pickup_datetime` and `lpep_dropoff_datetime` columns are in the format timestamp (date and hour+min+sec) and not in date.

- 15612

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/1b85ccff-23e7-4711-b10c-d3043378d59a)


<h3>Question 4. Longest trip for each day</h3>

Which was the pick up day with the longest trip distance? Use the pick up time for your calculations.

- 2019-09-26

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/b937b051-3072-4aa9-b87b-06ae3be9987d)
