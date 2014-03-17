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

## History of BatchRun

This is a project in GoogleCode, if you are interested in the old code, you can find it [here](https://code.google.com/p/batchrun/).

In the first edtion of this project, I use pp to control processes. In this lastest version, pp is not used anymore. Standard library is quite enough for this project.

I am trying to prettify the output by adding Pid in front of the output, but I cannot work it out. If anyone can improve this, I will be very appreciated. 
