## About
Curated requirements files for installing Python packages across multiple repos.

Change requirements once in this repo, and they will propagate to all repos that point here, on their next Docker build. 


## Usage

In your Dockerfile, add:

```
RUN pip3 install --upgrade pip

# Install common requirements
RUN wget -O requirements-snowflake-python3-10.txt https://raw.githubusercontent.com/patterninc/python-shared-requirements/master/requirements-snowflake-python3-10.txt
RUN pip3 install -r requirements-snowflake-python3-10.txt

# Install project-specific requirements
RUN pip3 install -r requirements.txt
```
