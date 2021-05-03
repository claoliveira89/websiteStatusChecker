## 72. Go Routines
- GO routine: a process that exists inside of the running program; it executes the code line by line;
- 'go': inside of our code, means to run the function or the block of code as a new go routine inside of the main go routine;
- Syntax of 'go routines':

        $ go checkLink(link)

- go: create a new thread go routine ...
- checkLink(link): ... and run this function with it;

## 73. Theory of Go Routines
- Eventhough we are starting different go routines at the same time, only one is executing at each time!
- 'go scheduler': monitors the code that is running inside of each 'go routine';
- ''go scheduler': schedulers runs one routine until it finishes or makes a blocking call (such as an HTTP request);
- One CPU core is only running the code of one go routine at the time;
- If there's more than one CPU core, by default Go tries to use one core! But this is easily changed: scheduler runs one thread on each "logical" core.
- Concurrency is not parallelism:
    - concurrency: we can have multiple threads executing code. If one thread blocks, another one is picked up and worked on.
    - parallelism: multiple threads executed at the exact same time. Requires multiple CPU's;

> OUR RUNNING PROGRAM
>
>> Main routine
> 
>> Child go routine
>
>> Child go routine
>
>> Child go routine
> -------------------------

- Main routine created when we launched our program
- Child routines created by the 'go' keyword

## 74. Channels
- Channels are used to communicate in between different running go routines;
- Channels are typed (string. int, etc): the data/messages that we send through the channels must be of the same type corresponding to however we created the channel;

## 76. Blocking Channels
- Receiving message from a channel is a blocking thing/ blocking line of code;

## 78. Repeating Routines
- infinite loop:

        for {

        }

