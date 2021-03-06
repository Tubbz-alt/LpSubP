# Legeonella pneumophila Subtyping Pipeline(LpSubP)

You can run pipeline through 

1) Clone git repository 

2) Dockerimage without clone repository

## Getting Started for github

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

module load Python/3.7

module load ncbi-blast+/LATEST

module load muscle/3.8.425

module load raxml/8.2.9

module load Entrez/E-utilities

module load prodigal/2.63

pip install -r requirements.txt --user

## Quick Start for Git


``` 
git clone https://github.com/CDCgov/lpsubp.git

cd ~/lpsubp/

python pipe1.py ~/50scheme/test1/

```

## Quick start for Dockerfile

### singularity

``` 

module load singularity

singularity pull docker://supark87/dockerfile_gittest

singularity run -B $(pwd)/inputfile/://data/inputfile/(space here)dockerfile_gittest.simg(spacehere)//data/inputfile

``` 

### Docker

``` 

docker pull supark87/dockerfile_gittest

docker run -it -v $(pwd)/inputfile/:/data/inputfile/ supark87/dockerfile_gittest /data/inputfile/ "your email inside of quotes"


``` 




This script runs entire pipeline from the beginning and get all output results

*base_dir: type 'pwd' in your home directory(i.e./scicomp/home/youruserid/) 

There would be "outputfile" directory at the end of pipeline under
"your_home_directory/your_genome_directory" (i.e./scicomp/home/youruserid/test1/outputfile/)

There would be myscript.log in your home directory that you can check when the pipeline started, each step completed, and finished. 


## Authors

Subin Park

APHL fellow at Centers for Disease control and Prevention

Phone : +1 470 725 5110
Email :nej1@cdc.gov

## Public Domain 

This repository constitutes a work of the United States Government and is not subject to domestic copyright protection under 17 USC § 105. This repository is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the CC0 1.0 Universal public domain dedication. All contributions to this repository will be released under the CC0 dedication. By submitting a pull request you are agreeing to comply with this waiver of copyright interest.

## License Standard Notice 

The repository utilizes code licensed under the terms of the Apache Software License and therefore is licensed under ASL v2 or later.
This source code in this repository is free: you can redistribute it and/or modify it under the terms of the Apache Software License version 2, or (at your option) any later version.
This source code in this repository is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the Apache Software License for more details.
You should have received a copy of the Apache Software License along with this program. If not, see http://www.apache.org/licenses/LICENSE-2.0.html
The source code forked from other open source projects will inherit its license.

## Privacy Standard Notice

This repository contains only non-sensitive, publicly available data and information. All material and community participation is covered by the Surveillance Platform Disclaimer and Code of Conduct. For more information about CDC's privacy policy, please visit http://www.cdc.gov/privacy.html.


All comments, messages, pull requests, and other submissions received through CDC including this GitHub page are subject to the Presidential Records Act and may be archived. Learn more at http://www.cdc.gov/other/privacy.html.

## Records Management Standard Notice

This repository is not a source of government records, but is a copy to increase collaboration and collaborative potential. All government records will be published through the CDC web site.

## Additional Standard Notices

Please refer to CDC's Template Repository for more information about contributing to this repository, public domain notices and disclaimers, and code of conduct.
