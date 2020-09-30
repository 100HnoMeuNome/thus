# Trend Micro Hybrid Cloud Security Command Line Interface (thus)

## OS specific install steps

As operating system update and versions move, this document's command may become dated. 

### Amazon Linux 

On Amazon linux, we need to specify python 3.6 on the yum command line. We can do python and jq at the same time.

`sudo yum install python36 jq -y`

Next install thus using pip

`pip-3.6 install tm-thus --user`

Lastly, configure thus

`thus --config`

### Amazon Linux 2 and Red Hat 8

On Amazon linux 2, we need to specify python 3 on the yum command line. We can do python and jq at the same time. 
It is the same for both Arm and Intel processors.

`sudo yum install python3 jq`

Next install thus using pip

`pip3 install tm-thus --user`

Lastly, configure thus

`thus --config`

### Ubuntu 20

Ubuntu 20 needs an apt update for pip3 to become available. 

`sudo apt update`

`sudo apt install python3-pip jq`

Next install thus using pip

`pip3 install tm-thus --user`

Note: You may need logout and back in for PATH updates to include thus 

Lastly, configure thus 

`thus --config`

### Suse SLES 12

On Suse 12, we need to install python 3.6 and pip. Then install thus using the newer python.  

`sudo zypper install python36 `

`curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`

`python3.6 get-pip.py`

To obtain jq, you will need to download it. At the time of this writing no package is available in zypper.
 
`curl https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64 -Lo jq `

`chmod a+x jq`

`sudo mv jq /usr/bin`

Next install thus using pip

`python3.6 -m pip install tm-thus --user`

Lastly, configure thus 

`thus --config`

### Windows

Download and install the latest python 3.x for Windows from [python.org](https://www.python.org/downloads/windows/) 

- Click the box to Add Python to PATH

Start a power shell prompt and install thus

`pip install tm-thus`

Lastly, configure thus 

`thus --config`


