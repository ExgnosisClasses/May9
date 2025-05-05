# May 9 AI for Execs Lab

In this lab, you will explore the bleu and rouge metrics for NLP that are used in assessing performance in LLMs

---

## Login
The login information for you lab is in this directory. Lookup your ID on the accompanying image.
1. The URL is [https://my.ablazedesktop.com](https://my.ablazedesktop.com)
2. Password: TEKana2501

Log into your machine.

---

## Get the labs


Open a conda prompt (the instructor will demonstrate). You should be able to start the prompt from the start menu. Or you can start Anaconda-navigator and open one from there. 

To get the lab code, clone the lab from here [May9 Labs](https://github.com/ExgnosisClasses/May9.git)

To demonstrate, I have started up at the root of my D: drive, although you can do this anywhere. Change into the cloned directory. Note that you will see a different number objects being downloaded

```base
D:\>git clone https://github.com/ExgnosisClasses/May9.git
Cloning into 'May9'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.

D:\>cd  May9

D:\May9>

```
---


## Virtual Environment

To install the correct versions of the libraries we will be using a virtual environment with a specific version of python, in this case version 3.11. I have not tested the labs with a more recent version, but I did notice that some of the libraries seemed only to be tested up to version 3.11

Create a directory somewhere you can use. In the code below, I have created it at `d:\May9

In the conda command prompt, create the virtual environment with the following command. Answer "y" whenever prompted.

 ```bash
D:\May9> conda create  --name=may9 python=3.11
Retrieving notices: done
Channels:
 - defaults
Platform: win-64
Collecting package metadata (repodata.json): done
Solving environment: done
...
```
Activate the environment.

```bash
D:\May9>conda activate may9

(may9) D:\May9>
```

Now we need to install all the packages we need.

```
(may9) D:\May9>pip install evaluate nltk rouge-score absl-py sacrebleu
...
...
Installing collected packages: pywin32, pytz, xxhash, urllib3, tzdata, typing-extensions, tabulate, six, regex, pyyaml, pyarrow, propcache, portalocker, packaging, numpy, multidict, lxml, joblib, idna, fsspec, frozenlist, filelock, dill, colorama, charset-normalizer, certifi, attrs, aiohappyeyeballs, absl-py, yarl, tqdm, sacrebleu, requests, python-dateutil, multiprocess, click, aiosignal, pandas, nltk, huggingface-hub, aiohttp, rouge-score, datasets, evaluate
Successfully installed absl-py-2.2.2 aiohappyeyeballs-2.6.1 aiohttp-3.11.18 aiosignal-1.3.2 attrs-25.3.0 certifi-2025.4.26 charset-normalizer-3.4.2 click-8.1.8 colorama-0.4.6 datasets-3.5.1 dill-0.3.8 evaluate-0.4.3 filelock-3.18.0 frozenlist-1.6.0 fsspec-2025.3.0 huggingface-hub-0.30.2 idna-3.10 joblib-1.5.0 lxml-5.4.0 multidict-6.4.3 multiprocess-0.70.16 nltk-3.9.1 numpy-2.2.5 packaging-25.0 pandas-2.2.3 portalocker-3.1.1 propcache-0.3.1 pyarrow-20.0.0 python-dateutil-2.9.0.post0 pytz-2025.2 pywin32-310 pyyaml-6.0.2 regex-2024.11.6 requests-2.32.3 rouge-score-0.1.2 sacrebleu-2.5.1 six-1.17.0 tabulate-0.9.0 tqdm-4.67.1 typing-extensions-4.13.2 tzdata-2025.2 urllib3-2.4.0 xxhash-3.5.0 yarl-1.20.0

(may9) D:\May9>
```

Now install Jupyter and register the kernel then start Jupyter lab. You should be redirected to the web page.

````bash
(may9) D:\May9>pip install jupyter
Collecting jupyter
....
(may9) D:\May9>python -m ipykernel install --user --name may9 --display-name "Lab"
Installed kernelspec may9 in C:\Users\micro\AppData\Roaming\jupyter\kernels\may9

(may9) D:\May9>jupyter lab
````
