# CS131 Project Sample Grading Script
 This is not really a grading script, rather, this is the simplest version of a super client (who has the power of starting a server)

## Background
- This is for [UCLA CS131 (**Programming Languages**)](http://web.cs.ucla.edu/classes/fall19/cs131/index.html) [**Project**](http://web.cs.ucla.edu/classes/fall19/cs131/hw/pr.html) (instructor: [Prof. Paul Eggert](http://web.cs.ucla.edu/classes/fall19/cs131/mail-eggert.html))
- This project is on Python, specifically aiming at the use of [asyncio](https://docs.python.org/3/library/asyncio.html) and [aiohttp](https://aiohttp.readthedocs.io/en/stable/)
- To complete the project a Google Map API Key is needed, I tried, in order to get rid of the limit you need payment information attached.

## Resource
- Thanks to previous-year TA, Wenhao's code
- Following [discussion online](https://stackoverflow.com/questions/3855127/find-and-kill-process-locking-port-3000-on-mac), to kill the process occupying port 8000 we could run: 
    ```shell
    lsof -ti:8000 | xargs kill
    ```
- To run a script in the background I used *nohup*
- To execute [command line within Python](https://stackoverflow.com/questions/450285/executing-command-line-programs-from-within-python):
    ```shell
    import os
    os.system('sox input.wav -b 24 output.aiff rate -v -L -b 90 48k')
    ```
- under [resources](./resources) folder I put my hint code for you to get started with this project there.

## Usage
* put your server.py under the **sample_submission** folder
* modify the port number from evaluation.py (or keep them the same if you run on local machine --- the easiest way to test your code is to change your port number to around 800X and then test them on your local machine)
* could run single evaluation by
    ```shell
    python client_basic.py
    ```
* I think it should work for mac and linux, probably won't work on Windows
* Probably a little bit adaptation is needed, probably the version matters