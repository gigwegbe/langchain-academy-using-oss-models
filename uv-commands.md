## UV COMMANDS

- Create a project: 
```
uv init quickstart-langchain-essentials
```
Directory structure: 
```
.
├── main.py
├── pyproject.toml
└── README.md

1 directory, 3 files
```

- Create a project with a specfic python version: 
```
 uv init  quickstart-langchain-essentials --python 3.11
```


- Managing project dependencies
```
uv add -r requirements.txt 
```

Output: 
```
george@Georges-MacBook-Pro quickstart-langchain-essentials % uv add -r requirements.txt 
Using CPython 3.11.6 interpreter at: /usr/local/bin/python3.11
Creating virtual environment at: .venv
Resolved 183 packages in 3.09s
      Built forbiddenfruit==0.1.4
⠙ Preparing packages... (69/81)
openai     ------------------------------ 896.00 KiB/998.72 KiB
langchain-classic ------------------------------ 872.56 KiB/1016.31 KiB
pydantic-core ------------------------------ 840.56 KiB/1.81 MiB
sqlalchemy ------------------------------ 907.00 KiB/2.03 MiB
widgetsnbextension ------------------------------ 874.67 KiB/2.09 MiB
langchain-community ------------------------------ 848.00 KiB/2.42 MiB
jsonschema-rs ------------------------------ 880.00 KiB/3.65 MiB
numpy      ------------------------------ 896.00 KiB/5.11 MiB
grpcio-tools ------------------------------ 848.00 KiB/5.57 MiB
cryptography ------------------------------ 896.00 KiB/6.36 MiB
jupyterlab ------------------------------ 888.56 KiB/11.81 MiB
notebook   ------------------------------ 875.00 KiB/13.79 MB                                                                                                                     
```

Directory structure: 
```
.
├── main.py
├── pyproject.toml
├── README.md
├── requirements.txt
└── uv.lock

1 directory, 5 files
```

Note that the virtual environment has already been created in the directory: 
```
george@Georges-MacBook-Pro quickstart-langchain-essentials % ls -la
total 1280
drwxr-xr-x@ 9 george  staff     288 Nov 20 12:48 .
drwxr-xr-x@ 8 george  staff     256 Nov 20 12:42 ..
-rw-r--r--@ 1 george  staff       5 Nov 20 12:42 .python-version
drwxr-xr-x@ 9 george  staff     288 Nov 20 12:49 .venv
-rw-r--r--@ 1 george  staff     109 Nov 20 12:42 main.py
-rw-r--r--@ 1 george  staff     420 Nov 20 12:48 pyproject.toml
-rw-r--r--@ 1 george  staff       0 Nov 20 12:42 README.md
-rw-r--r--@ 1 george  staff     178 Nov 20 12:46 requirements.txt
-rw-r--r--@ 1 george  staff  636933 Nov 20 12:48 uv.lock
george@Georges-MacBook-Pro quickstart-langchain-essentials % 
```
- To activate it(For old timers who don't learn new tricks 👴👵): 
```
george@Georges-MacBook-Pro quickstart-langchain-essentials % source .venv/bin/activate
(quickstart-langchain-essentials) george@Georges-MacBook-Pro quickstart-langchain-essentials % 
```

- To see the dependencies: 
```
(quickstart-langchain-essentials) george@Georges-MacBook-Pro langchain-academy-using-oss-models % uv pip  list 
Using Python 3.11.6 environment at: quickstart-langchain-essentials/.venv
Package                                  Version
---------------------------------------- -----------
aiohappyeyeballs                         2.6.1
aiohttp                                  3.13.2
aiosignal                                1.4.0
annotated-types                          0.7.0
anthropic                                0.74.1
anyio                                    4.11.0
appnope                                  0.1.4
argon2-cffi                              25.1.0
argon2-cffi-bindings                     25.1.0
arrow                                    1.4.0
asttokens                                3.0.1
async-lru                                2.0.5
attrs                                    25.4.0
babel                                    2.17.0
beautifulsoup4                           4.14.2
bleach                                   6.3.0
blockbuster                              1.5.25
certifi                                  2025.11.12
cffi                                     2.0.0
charset-normalizer                       3.4.4
click                                    8.3.1
cloudpickle                              3.1.2
```

Fun fact, your virtual environment might stop working one random day like today, my jupyter lab stopped working:
Remove the current env:  
```
rm -rf .venv
```
Get a fresh one: 
```
uv sync
```
It is easy. 

That is all the command you need for now. More would be add if necessary. 