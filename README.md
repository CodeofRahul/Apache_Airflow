# Apache_Airflow
This repo implements the idea of programmatically authoring, scheduling, and monitoring data pipelines as code, leveraging Apache Airflow's extensible Python framework to connect with diverse technologies and providing a web interface for workflow management, deployable from local setups to large-scale distributed environments.

![image](https://github.com/user-attachments/assets/ce2d490b-2b44-455a-9a00-08614472ef9a)

![image](https://github.com/user-attachments/assets/d642af5e-3645-4078-944a-decb77e3286b)

![image](https://github.com/user-attachments/assets/3b930166-0e63-451f-a30c-7b581ea675ec)

![image](https://github.com/user-attachments/assets/c11cc590-5e6b-49ee-ab8b-b1fea95523b8)

![image](https://github.com/user-attachments/assets/b96e1da8-5531-47a8-a9b6-8b41139bb96e)

![image](https://github.com/user-attachments/assets/faa2cd3d-527c-4bc8-845f-971ebc7615aa)

![image](https://github.com/user-attachments/assets/e96a7bf2-674c-4266-b759-2d33fd2418c8)

![image](https://github.com/user-attachments/assets/f2a51e02-0dd8-4d44-ada0-c3e9f2a78a51)

![image](https://github.com/user-attachments/assets/f7e73dbc-c292-45ca-88ad-581652ff08f1)

![image](https://github.com/user-attachments/assets/bec0d4a7-85be-481e-abf7-3b3f6717d1d2)

![image](https://github.com/user-attachments/assets/b44d93d4-0c20-499b-9dae-5c6447f46e1e)

![image](https://github.com/user-attachments/assets/af887da9-45c5-4a5f-bb0d-ea64cfd85786)

![image](https://github.com/user-attachments/assets/efc35c68-3ba6-4361-98b9-2a8764857df2)

![image](https://github.com/user-attachments/assets/6a0f61a6-7b97-4228-93d0-d328edab6fd3)

![image](https://github.com/user-attachments/assets/f3562885-c693-4454-a3ad-00437763e616)

![image](https://github.com/user-attachments/assets/9ee4fb8f-b6ed-49c5-a067-982eb8db16a5)


### **UV Commands:**

- `uv run filename.py`: To run a Python script.
- `pip install uv`: To install uv from PyPI.
- `uv --version`: Check the installed UV version.
- `uv venv`: Create a new virtual environment.
- `.venv\Scripts\activate`: Activate the virtual environment (Windows).
- `uv add <package_name>[==<version>]`: Adds dependency to your project's `pyproject.toml` and installs it into the active virtual environment(e.g., uv add flask==2.1.0).
- `uv add -r requirements.txt`: Add all dependencies from `requirements.txt`.
- `uv remove <package_name>`: Removes a dependency from `pyproject.toml` and uninstalls it 
- `deactivate`: Deactivate the virtual environment.
- `uv sync`: to manually update the environment
- `uv lock`: to lock the environment & updates the lock file



## **Creating a new project**

- You can create a new Python project using the uv init command:

```
uv init hello-world
cd hello-world
```

- Alternatively, you can initialize a project in the working directory:

```
mkdir hello-world
cd hello-world
uv init
```

uv will create the following files:

```
.
├── .python-version
├── README.md
├── main.py
└── pyproject.toml
```

The main.py file contains a simple "Hello world" program. Try it out with uv run:

```
uv run main.py
```

### Project structure

A project consists of a few important parts that work together and allow uv to manage your project. In addition to the files created by uv init, uv will create a virtual environment and uv.lock file in the root of your project the first time you run a project command, i.e., uv run, uv sync, or uv lock.

A complete listing would look like:

```
.
├── .venv
│   ├── bin
│   ├── lib
│   └── pyvenv.cfg
├── .python-version
├── README.md
├── main.py
├── pyproject.toml
└── uv.lock
```

The `pyproject.toml` contains metadata about your project:

```pyproject.toml

[project]
name = "hello-world"
version = "0.1.0"
description = "Add your description here"
readme = "README.md"
dependencies = []
```

You'll use this file to specify dependencies, as well as details about the project such as its description or license. You can edit this file manually, or use commands like uv add and uv remove to manage your project from the terminal.


### **Docs:**

- **Apache Airflow Docs:** https://airflow.apache.org/docs/apache-airflow/stable/index.html
- **UV installation:** https://docs.astral.sh/uv/getting-started/installation/
- **UV Docs :** https://docs.astral.sh/uv/#installation



### Problem

while running `git add.` getting this error:

```
warning: could not open directory 'logs/scheduler/latest/': Function not implemented
```

### Solution

- Create or edit the `.gitignore` file in the root of your Git repository.

- Add the following line to the `.gitignore` file:

```
logs/
```

- Save the file and then try `git add .` again.

