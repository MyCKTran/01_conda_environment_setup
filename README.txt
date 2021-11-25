This document is used for downloading, installing, and setting a conda environment by command lines in Ubuntu operation system (OS)
Note: 
     + Command lines in this document is in double quotes ("")
     + Names of file/object in this document is in single quote ('')
     + Setting in MAC OS may be different a little bit

Step 1:  Download 
         + Download the Anaconda package at the link: 'https://www.anaconda.com/products/individual#linux'
         + Assume that the Anaconda package of 'Anaconda3-2021.11-Linux-x86_64.sh' (for Ubuntu) or 'Anaconda3-2021.11-MacOSX-x86_64.sh' (for MAC) will be downloaded and stored at the directory of '/home/<user>/Download' (e.g. '/home/phaml/Download')


Step 2: Install (If using MAC, the name of conda package is different)
         + Open a terminal (at desktop or anywhere), and go in to the directory '/home/phaml/Download' by the command line:  "cd /home/phaml/Download"
         + Change the mode of the Anaconda package by the command line:  "chmod +x Anaconda3-2021.11-Linux-x86_64.sh"
         + Install the Anaconda package by the command line:  "./Anaconda3-2021.11-Linux-x86_64.sh"
         + Note that please insert 'y' or  'yes' to accept license agreement.
                     if we accept to active conda base environment during setting, when we open a terminal, the conda base environment will be activated immediately.
                     if we do not  accept to active the conda base environment during setting, when we open a terminal, we need to activate the conda base environment by the command line: "conda activate" 
         + After installing, using the command line "which conda" to check whether install process is done (i.e. "which <commmand>" is the command line to check whether a 'command/tool' is available or not)


Step 3: Create a new conda environment
         + Open a terminal
         + Activate the conda base environment by the command line:  "conda activate" (we can see:  '(base) phaml@s3ls2001' at the terminal that proves we are in the conda base environment). In case that activate the conda base environment is already (mentioned in the step 2), when a terminal is opend, the conda base environment is already activated.
         + Create a new environment by the command line:  "conda create --name py36 python=3.6"
           Note that the new environment has name of 'py36' with python version 3.6 is set up. (The version of python can be changed)
           Insert 'y' or 'yes' during install
         + After the install process finished, use the comman line: "conda info --envs" to check whether the new environment with name of 'py36' is available.
         + Access the new environment by the command line:  "conda activate py36". (Note that the name of 'py36' need to be typed exactly).
         + When we are in the 'py36' environment (Note that we can see:  '(py36) phaml@s3ls2001:' at the terminal that proves we are in this environment), we can further install the other libraries
           For example: Install 'numpy' library by the command line: "conda install -c anaconda numpy". Check the command lines for installing new libraries at 'https://anaconda.org/anaconda/numpy'
           
   

Step 4: Some basic command lines 
         (1) "conda activate"    : Acitvate the base environment
         (2) "conda activate <conda environment name>"    : Acitvate an conda environment with a certain nam (note that this environment has to be set up before)
         (3) "conda deactivate"  : Deactive or exit  an conda environment. (If we are in 'base' environment, this command line helps to exit the 'base' environment)
         (4) "conda info --envs" : Check all conda environments 
         (5) "conda list"        : List all library which were installed in the current conda environment
         (6) "conda env remove --name <conda environment name>" : Remove a conda environment with a certain name (note that this environment has to be set up before). After this command line, using the command line (4) to check whether the conda environment was deleted?
         (7) In case that we want to install a list of library, we create a file 'requirement.txt' in which list of libraries and version are define. 
             Then, run the command line "conda create --name py36 --channel conda-forge --file requirement.txt"
         (8) Check python  version:  "python --version"    
             
             
