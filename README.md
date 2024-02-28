## About
A collection of requirements files for installing Python packages, curated by Philip Huebner.

> [!IMPORTANT]  
> I never update a requirements file once it is released. 
> I only create new files.
> I am only taking responsibility for ensuring a file works properly at the time of release.
> If newer versions of a package are needed, contact me to create a new shared requirements file, or point your code to a newer file, if it exists. 


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
