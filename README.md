# Django Healthy_Helper

### pip install
    install required dependancies
Download all required packages in requirements/ using "pip install -r requirements/dev.txt"
If any errors occur (looking for missing .c files) "sudo apt install libpq-dev"

###########################
### DATABASE
	Default mysql to utf-8

Open the /etc/mysql/my.cnf MySQL configuration file in your favorite editor and
ensure that the following settings are set in the [client], [mysql], and [mysqld]
sections, as follows:

-------------
[client]<br />
default-character-set = utf8<br />

[mysql]<br />
default-character-set = utf8<br />

[mysqld]<br />
collation-server = utf8_unicode_ci<br />
init-connect = 'SET NAMES utf8'<br />
character-set-server = utf8<br />

-------------

/etc/init.d/mysql restart


###########################
### Best practises 
#### import structure 
    Use the following structure for each Python file that you are creating. Categorize the
    imports into sections, as follows:
##### System libraries
import os<br />
import re<br />

from datetime import datetime
##### Third-party libraries
import boto<br />
from PIL import Image<br />
##### Django modules
from django.db import models<br />
from django.conf import settings<br />
##### Django apps
from cms.models import Page<br />
##### Current-app modules
from .models import NewsArticle<br />
from . import app_settings<br />


###########################
