## What are SSL errors.?

SSL errors are connection errors to a secured HTTPS website. Medusa uses this method to ensure your connection is secure and private. However that also means you need to have a recent OpenSSL version installed on your OS. If its outdated you can suffer from SSL connection errors.  

Some examples of SSL errors : 

```
POSTPROCESSER :: Boxcar2 notification failed.error ('_ssl.c:574: The handshake operation timed out',) [3f0efd1]
```  

```
POSTPROCESSER :: Boxcar2 notification failed.error EOF occurred in violation of protocol (_ssl.c:590) [3f0efd1]
```  

```
Postprocessing fails with SSL: CERTIFICATE_VERIFY_FAILED
```  
```
[NZBGeek] :: Connection error to getURL https://api.nzbgeek.info/api?apikey=*KEY REMOVED*&tvdbid=262765&season=3&maxage=500&cat=5030%2C5040&q=The.Valleys&limit=100&t=tvsearch&offset=0&ep=7 Error: u'error (\'Connection aborted.\', BadStatusLine("\'\'",))' [4423fe9] 
```  
```
 _ssl.c:499: error:14077438:SSL routines:SSL23_GET_SERVER_HELLO:tlsv1 alert internal error
```  
```
[TvChaosUK] :: [d775a91] Traceback (most recent call last): AAAttributeError: '_socketobject' object has no attribute 'set_tlsext_host_name'
```


## What versions should i use.?

We advice to use a minimum of OpenSSL version 1.01e. Versions below this dont support TLS1.1 or TLS1.2 that is needed for a site like thepiratebay.  
Additionally we advice to use Python v 2.7.10 as that includes a recent version that works fine with SSL.

**Summery :**  

* Python < 2.7.9 needs a working pyOpenSSL to handle SNI and certificate verification. 
* You have pyOpenSSL > v0.13.1 and do not have the Python cryptography module installed so you have no SNI, and are trying to access a site on shared hosting
* Your system OpenSSL version is less than 1.0.1e and you are trying to access a site using TLS1.1 or TLS1.2 

## How can i see what version i have installed.?

If you browse to the `Help & Info` page (screenshot below) inside Medusa, you can check the field `Python Version:` & `SSL Version:`.
Those will show you the version currently in use by Medusa/OS.   

![helpinfo](https://cloud.githubusercontent.com/assets/7928052/13013132/70b0840c-d1ae-11e5-8894-f3dd8b95dfe9.png)

## How would i fix an SSL error.?

There are multiple way's. But the most obviously is update your OpenSSl & Python versions. Some [Solutions](https://github.com/pyMedusa/SickRage/wiki/SSL-Errors#solutions) you find below.  

However you might be in a situation where you have and old device and updating isn't possible. Than there are some work-around's , but we advice to use them as a last resort as they aren't the best practice.

* Go to Settings --> General --> Advanced Settings. And disable the function `Verify SSL Certs`. This will prevent the checking if an certificate is valid or not.  
* Change the URL(s) from `https` to `http`. Most providers have a custom URL field, so just enter the `http` URL there. Same for the notifiers etc. However be aware that you are not using a secure connection then.  

== 
___




### Solutions


1. Make sure you have OpenSSL 1.0.1e or newer. Check with `openssl version`. Google how to upgrade OpenSSL on your system.

2. Install Python 2.7.10 and remove pyOpenSSL, or Downgrade pyOpenSSL to 0.13.1 or install missing modules.

a. Downgrade pyOpenSSL (Best/Easiest Solution, should work on all platforms with apt)
```
sudo apt-get install --reinstall build-essential python-pip python-dev libssl-dev libffi-dev
sudo pip2.7 install -U setuptools pip pyasn1 ndg-httpsclient pyopenssl==0.13.1
```

b. Install the Python cryptography module (PITA, Does not work on all platforms)
This will build and install all of the packages needed to use pyOpenSSL from Medusa:
```
sudo apt-get install build-essential python-pip python-dev libffi-dev libssl-dev
wget https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py -O - | sudo python2
sudo pip install -U cryptography ndg-httpsclient pyopenssl
```

### Why don't we just include the correct version of pyOpenSSL?
* Architecture. pyOpenSSL compiles some shared objects when installed, and for example x64 .so files will not work with x86 and vice versa, or other architectures.


### Notes

* The wget line is because some distributions do not even have setuptools available.
* Some platforms have a funky wget, if you have problems with the wget command do this in place of that step: 
```
curl http://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py -O -L
sudo python2 ez_setup.py
```
* `urllib3` does not run using `pyopenssl` unless `ndg-httpsclient`, `pyasn1`, and `pyopenssl` modules are installed, it runs with the standard `ssl` built into python. The other packages, and libraries, are dependencies or build dependencies for upgrading some python packages.

Sometimes a user that just migrated from sickbeard asks the question `I never had any issues with sickbeard` Well that's because sickbeard didn't use secure connections at all...  

### Please add any platform specific instructions for completing these tasks below
