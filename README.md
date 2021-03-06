Cosmic Praise
=============

Simulator and lighting code for Cosmic Praise

http://douglasruuska.com/cosmic-praise


Quickstart
----------

1. Install dependencies

  ```
  sudo pip install colormath 
  sudo pip install python-rtmidi --pre
  ```
  
2. Run the simulator (pre-built for OSX; Linux binaries might be available soonish; you can get the source and build yourself from our OPC fork here: https://github.com/Dewb/openpixelcontrol) 

  ```
  simulator/osx-10.9/gl_server layouts/cosmicpraise.json
  ```

3. Run the client code to send pixels to the simulator:

  ```
  python client/python/cosmicpraise.py -l layouts/cosmicpraise.json -f 60 --sim
  ```

Virtual Environment
-------------------

Virtual environments provide a nice method for keeping python projects locally
managed and seperate from the system.  It's easy to have multiple virtual
environments that provide different versions of the runtime, making it ideal
for development.

If you don't have virtualenv installed, you will need to install it the first time:

```
$ sudo pip install virtualenv
```

Once you have virtualenv installed, you will need to bootstrap your environment:

```
$ virtualenv $HOME/local/cosmic-praise
$ . $HOME/local/cosmic-praise/bin/activate
(cosmic-praise)$ easy_install -U setuptools
(cosmic-praise)$ pip install colormath numpy
(cosmic-praise)$ pip install python-rtmidi --pre
```

When you are done with your virtual environment, either logout, or run deactivate:

```
(cosmic-praise)$ deactivate
$
```
