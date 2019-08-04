
# PyCoin
PyCoin is a cryptocurrency app, made using Python and Flask. It's an API that helps with better understanding how the block-chain technology works. You are able to send and receive coins through different nodes, mine your own and connect to peer networks. It simulates how cryptocurrencies like Bit Coin work and overall it's a great tool for anyone who'd like to better understand the block-chain technology. 

# How to use
* Install [Python 3.7](https://www.python.org/downloads)
* Install Dependencies:
  * flask
  * flask_cors
  * pycryptodome

**Installing the packages**
`python -m pip install flask flask_cors pycryptodome` 

**Alternatives**
Use a 3rd party package installer like [Anaconda](https://www.anaconda.com/distribution)


**Steps for using Anaconda:**
   * Install it on your specific OS
   * Go to Environments
   * Create a new environment (name it whatever you wish)
   * Boot it up
   * Install the required packages using the Anaconda Navigator
   * After creating an environment, you need to activate it. There are two ways of doing that:
		* Execute source activate NAME_OF_ENVIRONMENT  (e.g. source activate pycoin ) on macOS and Linux or just activate NAME_OF_ENVIRONMENT  (e.g. activate pycoin ) on Windows. This might fail for Windows though. To fix it, please see [this thread.](https://github.com/ContinuumIO/anaconda-issues/issues/2533)

		* Alternatively, you use the Anaconda Navigator to launch a terminal/ command prompt that already uses your new virtual environment: Click on the green "play" button next to your environment name and choose the option to launch a new terminal/ command prompt there. This will be a normal terminal/ command prompt, so after navigating into your project folder (via the cd command), you can use it.

# Important
Please note that to run Python using the python command in Windows CMD you must first add it to the PATH environment variable, as explained [here](https://stackoverflow.com/questions/4621255/how-do-i-run-a-python-program-in-the-command-prompt-in-windows-7/4621277#4621277).

To execute Pip, first of all make sure you have it. So type in your CMD:
```console
> python
>>> import pip
>>>
```

# How the app works
`python node.py` is the basic command to start up the server on the default port 5000.
`python node.py -p PORT_NUMBER_HERE` eg: `python node.py -p 5001` will start up the server on a different port.
You can use this to set up several servers and have them act as nodes in order to transfer funds,mine blocks and connect to peer networks.

* First thing you need to do is **Create a new Wallet**, this will provide you with a Public and Private key, you only need to use the Public Key to receive funds. Alternatively you can load your wallet if you made one previously on that port.(Remember this all runs on localhost).
* Now you can mine coins, each time you mine you get 10 coins and all the open transactions get placed into the blockchain.
*  **Resolve Conficts** essentially makes sure that no node or server running on different ports has a different version of the blockchain, so it will update it accordingly, this applies to open transactions as well. 
*  **Load blockchain** to see all the transactions that have occured, who sent how much and to whom. 
* **Network** tab, this is important in order to be able to send and receive funds from peer networks(eg: localhost:5001 sends localhost:5000 20 coins), they are peer networks of each other, localhost:5000 has localhost:5001 as it's Peer Node and vice-versa.