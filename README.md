# Template for developing & deploying a Cloud Run Service

[Cloud Run introduction]

New Steps to Adapa:

1. Developing Step (Develop ingo local environment or VSCode in GCP)

    1.1 Set up the project environment

        1.1.1 Set up the python version with Pyenv

        bla bla bla

        1.1.2 Create the working directory

        ```
        mkdir ~/project_folder
        cd ~/project_folder
        ```

        1.1.3 Set up the virtual environment with Virtualenv

        Instalar virtualenv

        `pip3 --version`
        `pip3 install virtualenv`

        Create a VE with a specific python version (ADD /Users/vdjimenez/Library/Python/3.8/bin AS ON PATH)

        MacOs: `/Users/<user_name>/Library/Python/3.8/bin/virtualenv -p /Users/<user_name>/.pyenv/versions/3.9.10/bin/python3.9 venv`
        CloudShell: `virtualenv -p /home/<user_name>/.pyenv/versions/3.9.10/bin/python3.9 venv`

        1.1.Set up a Git project & push into a repository --> Add info from doc SetUp Cloud Source Repository

        `git init`
        `git config --global/--local user.name "<name>"`
        `git config --global/--local user.email "<email>"`
        `echo "# Title Project" >> README.md`
        `git add README.md`
        `git commit -m "v0.0 - Initialize repository"`
        `git branch -M main` (only for GitHub)
        `git remote add origin <URL_repository>`
        `git push -u origin main/master`

    1.2 Build the project

        1. Add `main.py` file
        2. Add `requirements.txt` file
        3. Add `Dockerile` file or `Procfile` file
        4. Add `.dockerignore` file
        5. Add `.gitignore` file
        6. Add `README.md`

    1.3 Debug the project

    ba bla bla
    
2. Deploying Step (Deploy into GCP)

    2.1 Enable the APIs

    From Cloud Shell, enable the Artifact Registry, Cloud Build, and Cloud Run APIs:

    ```
    gcloud services enable \
        artifactregistry.googleapis.com \
        cloudbuild.googleapis.com \
        run.googleapis.com
    ```

    2.2 Push the new release into the repository

    bla bla bla

    2.3 Create & run the trigger in Cloud Build

    bla bla bla

    2.4 Add the last configuration in the Cloud Run console 

    bla bla bla
