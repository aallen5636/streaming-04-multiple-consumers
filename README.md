# Name: Ashley Allen
# streaming-04-multiple-consumers

> Use RabbitMQ to distribute tasks to multiple workers

One process will create task messages. Multiple worker processes will share the work. 


## Before You Begin

1. Fork this starter repo into your GitHub.
1. Clone your repo down to your machine.
1. View / Command Palette - then Python: Select Interpreter
1. Select your conda environment. 

## Read

1. Read the [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)
1. Read the code and comments in this repo.

## RabbitMQ Admin 

RabbitMQ comes with an admin panel. When you run the task emitter, reply y to open it. 

(Python makes it easy to open a web page - see the code to learn how.)

-Username and pasword is guest/guest

## Execute the Producer

1. Run emitter_of_tasks.py (say y to monitor RabbitMQ queues)

v1 emitter:

<img width="953" alt="v1_emitter" src="https://user-images.githubusercontent.com/95989498/215904430-79fda38e-957e-49ce-a3e9-a87d0ecf90eb.png">

Explore the RabbitMQ website.

## Execute a Consumer / Worker

1. Run listening_worker.py

Will it terminate on its own? How do you know? 
  -listing_worker.py will not terminate on it's own. Additional code is not able to be completed until connection termination is executed. 

 v1 listeners:
 <img width="953" alt="v1_listening" src="https://user-images.githubusercontent.com/95989498/215904935-f5ac2d12-011f-4775-a609-d266ddaaf67d.png">

## Ready for Work

1. Use your emitter_of_tasks to produce more task messages.

## Start Another Listening Worker 

1. Use your listening_worker.py script to launch a second worker. 

Follow the tutorial. Add multiple tasks (e.g. First message, Second message, etc.)
How are tasks distributed? Tasks are rotated between two consumers that are currently open. 
Monitor the windows with at least two workers. 
Which worker gets which tasks? 

v2_emitter:
<img width="953" alt="v2_emitter" src="https://user-images.githubusercontent.com/95989498/215905463-738fe7da-89a7-4251-99f6-27db1c55a3d3.png">

v2_listeners
<img width="953" alt="v2_listening" src="https://user-images.githubusercontent.com/95989498/215905955-12743fb5-9094-4a2e-b9ef-408289f7382f.png">


## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)


## Screenshot

See a running example with at least 3 concurrent process windows here:

v1 and v2
<img width="336" alt="Concurrent Process" src="https://user-images.githubusercontent.com/95989498/215908508-4f22007a-a765-469e-8f5e-c162a72d1158.png">

v3
<img width="953" alt="V3 multiple terminals " src="https://user-images.githubusercontent.com/95989498/216741976-c55d8e8b-12fb-4b63-b273-9f5adc484a04.png">

