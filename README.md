# CSSLabs-Algorithms-Society


#### Instructions
- Go to this link: https://github.com/UM-CSS/CSSLabs-Algorithms-Society
- If you are familiar with `git`, we recommend you clone the repo.
- If you are unfamiliar with `git`, the easiest option is to follow these steps:
    - Press the ![Clone or download](images/clone_or_download.png "Clone or download") button on the right side of each repository.
    - Choose `Download ZIP` and save the file somewhere memorable.
    - Go to where the file is saved and unzip it.

## 1. Environment Setup <a name="setup"></a>
You will need some software to be able to run this code. We recommend the following:
1. Install [Docker Desktop](https://docs.docker.com/desktop/) on the laptop or desktop computer.  Here are direct links for various operating systems: [Mac OS](https://docs.docker.com/desktop/install/mac-install/), [Windows](https://docs.docker.com/desktop/install/windows-install/), [Linux](https://docs.docker.com/desktop/install/linux-install/). 
2. We are using [Jupyter notebook on Docker Stack](https://jupyter-docker-stacks.readthedocs.io/en/latest/) to avoid steps to install various components. With the Docker Desktop installed in above step, now we can load a docker container directly by:
    - Open a terminal on Mac OS or the Commandline Prompt on Windows, and **navigate to the folder where you downloaded the notebook in step 0**.

        - If you are a Mac user, run the following command:
        ```bash
        docker run -v $(pwd):/home/jovyan/CSSLabs -p 8888:8888 quay.io/jupyter/scipy-notebook:2024-01-05
        ```

        - If you are a Windows Command shell user, use this command:
        ```bash
        docker run -v %cd%:/home/jovyan/CSSLabs -p 8888:8888 quay.io/jupyter/scipy-notebook:2024-01-05
        ```

        - If you are a Windows PowerShell user, use the following command:
        ```bash
        docker run -v ${PWD}:/home/jovyan/CSSLabs -p 8888:8888 quay.io/jupyter/scipy-notebook:2024-01-05
        ```
    
    - The above step will first pulling the docker container from the remote repository.  You should see a list of layers of this container being pulled off the remote repo. Notice, the image pulling steps only happens when this is done for the first time.  Once the pulling is completed, it will run the container on your local operating system, and expose a port 8888 on your local host, with a token, i.e. ```b045...61e4``` in the following case.  

    ```
    ...
    aef40af6dc3e: Pull complete 
    3c01e088ac39: Pull complete 
    Digest: sha256:162744a05b15a0bcad1064238af48b0e4e6bcb56f1e4cc607f34343ee3a0f728
    Status: Downloaded newer image for quay.io/jupyter/scipy-notebook:2024-01-05
    Entered start.sh with args: jupyter lab
    Running hooks in: /usr/local/bin/start-notebook.d as uid: 1000 gid: 100

    ...

    [I 2024-01-05 21:07:36.315 ServerApp] Serving notebooks from local directory: /home/jovyan
    [I 2024-01-05 21:07:36.315 ServerApp] Jupyter Server 2.12.2 is running at:
    [I 2024-01-05 21:07:36.315 ServerApp] http://bda4c6f01885:8888/lab?token=b045793e8e725f79808eb241136cf80294ba94d86c8f61e4
    [I 2024-01-05 21:07:36.315 ServerApp]     http://127.0.0.1:8888/lab?token=b045793e8e725f79808eb241136cf80294ba94d86c8f61e4
    [I 2024-01-05 21:07:36.315 ServerApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
    [C 2024-01-05 21:07:36.317 ServerApp] 
        
        To access the server, open this file in a browser:
            file:///home/jovyan/.local/share/jupyter/runtime/jpserver-7-open.html
        Or copy and paste one of these URLs:
            http://bda4c6f01885:8888/lab?token=b045793e8e725f79808eb241136cf80294ba94d86c8f61e4
            http://127.0.0.1:8888/lab?token=b045793e8e725f79808eb241136cf80294ba94d86c8f61e4
    ```

3. If you see the above terminal completed with above output and waiting for input, congratulations! you have successfully installed docker container that  you need. If not, there is something wrong with your installation, and please ask one of the instructors for help.  Use a web browser to access the above URL with the token from your local machine, i.e. you have to copy the similar string from your output with your TOKEN string and replace following one. If not, you might be given a prompt to copy/paste the token on the first webpage. 
    ```
    http://127.0.0.1:8888/lab?token=xxx
    ```

4. In the jupyter lab environment we have created above, you should see a list of files and folders on the left of the webpage, and Notebook, Console, and Others to the right side of the page. Navigate through the left file browser to the `CSSLabs` folder.  In this folder is a list of lab files ending in `.ipynb`, stands for Interactive (i) Python (py) Notebook (nb). Click on any of these and they should open in a new Notebook tab with the lab code and instructions.
    - **Note** if you get an error or the top of the new page does not look like this 
        - ![notebook top](images/notebook_top.png "notebook top"), 
        - Then you have probably made a mistake in downloading the files. Go back to the "[Getting the Code and Data](#download)" instructions. 
5. If you are new to Jupyter Notebooks, everything you need for these labs is in the great [introduction to their basic use](http://nbviewer.jupyter.org/github/jupyter/notebook/blob/master/docs/source/examples/Notebook/Notebook%20Basics.ipynb).





