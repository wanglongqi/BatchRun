![](logo.png) BatchRun
========

Full use of your multi-core CPU by BatchRun.

## Usage

    Usage: batchrun.py [options] [InputFile(s)]

    Options:
        --version             show program's version number and exit
        -h, --help            show this help message and exit
        -n NCPU, --ncpu=NCPU  ncpu, use how many cpus for current job.
        -v                    verbosity, dupulicate v to get more details.
        InputFile(s)          If no file(s) is presented, input is readed from stdin.

Output from "batchrun.py -vvvv -n 4 testjobs >sample.out" is shown in [sample.out](sample.out)

First, all jobs will be listed. 

    Jobs 0 : sleep  0
    Jobs 1 : sleep  3
    Jobs 2 : sleep  1
    Jobs 3 : sleep  5
    Jobs 4 : sleep  4

Second, a comfirm message will be printed.

    Do you want to execute the jobs?(y/N) 

Third, jobs will be excuted. Status will be print to stdout.

    Executing job 0 , Pid is 9544
    :: New Job info :: 
     Command: sleep  0
         Start time: 3.20708e-07
     Job pid: 9544	Job count: 0
     
    Executing job 1 , Pid is 10760
    :: New Job info :: 
     Command: sleep  3
         Start time: 0.00558224
     Job pid: 10760	Job count: 1
     
    Job 0 Finished! Total time 0.324299 Sec.
    :: Finished Job info :: 
     Command: sleep  0
         Total time: 0.324317
     Job pid: 9544	Job count: 0
     
    Job 1 Finished! Total time 3.33273 Sec.
    :: Finished Job info :: 
     Command: sleep  3
         Total time: 3.33275
     Job pid: 10760	Job count: 1
  
If Ctrl + C is pressed in the middle, following message will be printed.

    Note: User Abort Determined!
    13 jobs has been submitted. Rest jobs will be abandoned.
    Submited job will not be affected. Kill the process if you will.


## History of BatchRun

This is a project in GoogleCode, if you are interested in the old code, you can find it [here](https://code.google.com/p/batchrun/).

In the first edtion of this project, I use pp to control processes. In this lastest version, pp is not used anymore. Standard library is quite enough for this project.

I am trying to prettify the output by adding Pid in front of the output, but I cannot work it out. If anyone can improve this, I will be very appreciated. 
