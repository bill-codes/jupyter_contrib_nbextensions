


Install on server without admin privilege
=============



```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>conda install -c conda-forge jupyter
_contrib_nbextensions
Fetching package metadata .......An unexpected error has occurred.
Please consider posting the following information to the
conda GitHub issue tracker at:

    https://github.com/conda/conda/issues



Current conda install:

               platform : win-64
          conda version : 4.3.8
       conda is private : False
      conda-env version : 4.3.8
    conda-build version : not installed
         python version : 3.6.0.final.0
       requests version : 2.12.4
       root environment : C:\ProgramData\Anaconda3  (writable)
    default environment : C:\ProgramData\Anaconda3
       envs directories : C:\ProgramData\Anaconda3\envs
          package cache : C:\ProgramData\Anaconda3\pkgs
           channel URLs : https://conda.anaconda.org/conda-forge/win-64
                          https://conda.anaconda.org/conda-forge/noarch
                          https://conda.anaconda.org/anaconda-fusion/win-64
                          https://conda.anaconda.org/anaconda-fusion/noarch
                          https://repo.continuum.io/pkgs/free/win-64
                          https://repo.continuum.io/pkgs/free/noarch
                          https://repo.continuum.io/pkgs/r/win-64
                          https://repo.continuum.io/pkgs/r/noarch
                          https://repo.continuum.io/pkgs/pro/win-64
                          https://repo.continuum.io/pkgs/pro/noarch
                          https://repo.continuum.io/pkgs/msys2/win-64
                          https://repo.continuum.io/pkgs/msys2/noarch
            config file : C:\Users\localusername\.condarc
           offline mode : False
             user-agent : conda/4.3.8 requests/2.12.4 CPython/3.6.0 Windows/2008
ServerR2 Windows/6.1.7601



`$ C:\ProgramData\Anaconda3\Scripts\conda-script.py install -c conda-forge jupyt
er_contrib_nbextensions`




    Traceback (most recent call last):
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\exceptions.py", lin
e 617, in conda_exception_handler
        return_value = func(*args, **kwargs)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\cli\main.py", line
137, in _main
        exit_code = args.func(args, p)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\cli\main_install.py
", line 80, in execute
        install(args, parser, 'install')
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\cli\install.py", li
ne 210, in install
        unknown=index_args['unknown'], prefix=prefix)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 120, in get_index
        index = fetch_index(channel_priority_map, use_cache=use_cache)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 445, in fetch_index
        repodatas = _collect_repodatas(use_cache, urls)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 433, in _collect_repodatas
        repodatas = _collect_repodatas_serial(use_cache, urls)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 401, in _collect_repodatas_serial
        for url in urls]
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 401, in <listcomp>
        for url in urls]
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 141, in func
        res = f(*args, **kwargs)
      File "C:\ProgramData\Anaconda3\lib\site-packages\conda\core\index.py", lin
e 391, in fetch_repodata
        with open(cache_path, 'w') as fo:
    PermissionError: [Errno 13] Permission denied: 'C:\\ProgramData\\Anaconda3\\
pkgs\\cache\\2116b818.json'
```




```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>pip install jupyter_nbextensions_con
figurator
Collecting jupyter_nbextensions_configurator
  Downloading jupyter_nbextensions_configurator-0.2.8-py2.py3-none-any.whl (465k
B)
    100% |████████████████████████████████| 471kB 701kB/s
Collecting jupyter-contrib-core>=0.3.3 (from jupyter_nbextensions_configurator)
  Downloading jupyter_contrib_core-0.3.3-py2.py3-none-any.whl
Requirement already satisfied: tornado in c:\programdata\anaconda3\lib\site-pack
ages (from jupyter_nbextensions_configurator)
Requirement already satisfied: traitlets in c:\programdata\anaconda3\lib\site-pa
ckages (from jupyter_nbextensions_configurator)
Requirement already satisfied: pyyaml in c:\programdata\anaconda3\lib\site-packa
ges (from jupyter_nbextensions_configurator)
Requirement already satisfied: jupyter-core in c:\programdata\anaconda3\lib\site
-packages (from jupyter_nbextensions_configurator)
Requirement already satisfied: notebook>=4.0 in c:\programdata\anaconda3\lib\sit
e-packages (from jupyter_nbextensions_configurator)
Requirement already satisfied: setuptools in c:\programdata\anaconda3\lib\site-p
ackages\setuptools-27.2.0-py3.6.egg (from jupyter-contrib-core>=0.3.3->jupyter_n
bextensions_configurator)
Installing collected packages: jupyter-contrib-core, jupyter-nbextensions-config
urator
Successfully installed jupyter-contrib-core-0.3.3 jupyter-nbextensions-configura
tor-0.2.8
```







```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>jupyter contrib nbextension install
--system
community-contributed spice for Jupyter Interactive Computing

Options
-------

Arguments that take values are actually convenience aliases to full
Configurables, whose aliases are listed on the help line. For more information
on full configurables, see '--help-all'.

--debug
    set log level to logging.DEBUG (maximize logging output)
--generate-config
    generate default config file
-y
    Answer yes to any questions instead of prompting.
--log-level=<Enum> (Application.log_level)
    Default: 30
    Choices: (0, 10, 20, 30, 40, 50, 'DEBUG', 'INFO', 'WARN', 'ERROR', 'CRITICAL
')
    Set the log level by value or name.
--config=<Unicode> (JupyterApp.config_file)
    Default: ''
    Full path of a config file.

To see all available configurables, use `--help-all`

[JupyterContribApp] CRITICAL | Bad config encountered during initialization:
[JupyterContribApp] CRITICAL | Unrecognized flag: '--system'
```






```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>jupyter contrib nbextension install
--user
community-contributed spice for Jupyter Interactive Computing

Options
-------

Arguments that take values are actually convenience aliases to full
Configurables, whose aliases are listed on the help line. For more information
on full configurables, see '--help-all'.

--debug
    set log level to logging.DEBUG (maximize logging output)
--generate-config
    generate default config file
-y
    Answer yes to any questions instead of prompting.
--log-level=<Enum> (Application.log_level)
    Default: 30
    Choices: (0, 10, 20, 30, 40, 50, 'DEBUG', 'INFO', 'WARN', 'ERROR', 'CRITICAL
')
    Set the log level by value or name.
--config=<Unicode> (JupyterApp.config_file)
    Default: ''
    Full path of a config file.

To see all available configurables, use `--help-all`

[JupyterContribApp] CRITICAL | Bad config encountered during initialization:
[JupyterContribApp] CRITICAL | Unrecognized flag: '--user'
```






 

```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>jupyter contrib nbextension install
--help-all
community-contributed spice for Jupyter Interactive Computing

Options
-------

Arguments that take values are actually convenience aliases to full
Configurables, whose aliases are listed on the help line. For more information
on full configurables, see '--help-all'.

--debug
    set log level to logging.DEBUG (maximize logging output)
--generate-config
    generate default config file
-y
    Answer yes to any questions instead of prompting.
--log-level=<Enum> (Application.log_level)
    Default: 30
    Choices: (0, 10, 20, 30, 40, 50, 'DEBUG', 'INFO', 'WARN', 'ERROR', 'CRITICAL
')
    Set the log level by value or name.
--config=<Unicode> (JupyterApp.config_file)
    Default: ''
    Full path of a config file.

Class parameters
----------------

Parameters are set from command-line arguments of the form:
`--Class.trait=value`. This line is evaluated in Python, so simple expressions
are allowed, e.g.:: `--C.a='range(3)'` For setting C.a=[0,1,2].

JupyterContribApp options
-------------------------
--JupyterContribApp.answer_yes=<Bool>
    Default: False
    Answer yes to any prompts.
--JupyterContribApp.config_file=<Unicode>
    Default: ''
    Full path of a config file.
--JupyterContribApp.config_file_name=<Unicode>
    Default: ''
    Specify a config file to load.
--JupyterContribApp.generate_config=<Bool>
    Default: False
    Generate default config file.
--JupyterContribApp.log_datefmt=<Unicode>
    Default: '%Y-%m-%d %H:%M:%S'
    The date format used by logging formatters for %(asctime)s
--JupyterContribApp.log_format=<Unicode>
    Default: '[%(name)s]%(highlevel)s %(message)s'
    The Logging format template
--JupyterContribApp.log_level=<Enum>
    Default: 30
    Choices: (0, 10, 20, 30, 40, 50, 'DEBUG', 'INFO', 'WARN', 'ERROR', 'CRITICAL
')
    Set the log level by value or name.
```







```
(C:\ProgramData\Anaconda3) C:\Users\adminusername>jupyter contrib nbextension install
--generate-config
Writing default config to: C:\Users\localusername\.jupyter\jupyter contrib_config.py

(C:\ProgramData\Anaconda3) C:\Users\adminusername>jupyter nbextensions_configurator en
able
Enabling: jupyter_nbextensions_configurator
- Writing config: C:\Users\localusername\.jupyter
    - Validating...
      jupyter_nbextensions_configurator  ok
Enabling notebook nbextension nbextensions_configurator/config_menu/main...
Enabling tree nbextension nbextensions_configurator/tree_tab/main...

(C:\ProgramData\Anaconda3) C:\Users\adminusername>
```





