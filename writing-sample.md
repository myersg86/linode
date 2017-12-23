---
author:
  name: Greg Myers
  email: greg@gregmyers.com
description: '.'
keywords: ["Hugo", "NGINX", "static website"]
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
published: 2017-12-22
modified: 2017-12-22
modified_by:
  name: Greg
title: 'Guide Title'
contributor:
  name: Your Name
  link: Github/Twitter/LinkedIn URL
external_resources:
  - '[Link Title 1](http://www.example.com)'
  - '[Link Title 2](http://www.example.net)'
---

## Before You Begin

1.  Familiarize yourself with our [Getting Started](https://linode.com/docs/linode-writers-formatting-guide/) guide and complete the steps for setting your Linode's hostname and timezone.

2.  This guide will use `sudo` wherever possible. Complete the sections of our [Securing Your Server](/docs/security/securing-your-server) to create a standard user account, harden SSH access and remove unnecessary network services.

3.  Update your system:

        sudo apt-get update && sudo apt-get upgrade
        
{{< note >}}
This guide is written for a non-root user. Commands that require elevated privileges are prefixed with `sudo`. If you’re not familiar with the `sudo` command, see the [Users and Groups](/docs/tools-reference/linux-users-and-groups) guide.
{{< /note >}}

-----

## Using MySQL

1.  Log in to MySQL as the root user:
        mysql -u root -p

2.  When prompted, enter the root password.

### Create a New MySQL User and Database

1.  In the example below, `testdb` is the name of the database, `testuser` is the user, and `password` is the user’s password.

        create database testdb;
        grant all on testdb.* to 'testuser' identified by 'password';

2.  Exit MySQL.

        exit

### Create a Sample Table

1.  Log back in as `testuser`:

        mysql -u testuser -p


**bold**
*italic*

Update your system:

    yum update
    
Update your system by running `yum update`.

Navigate to `/var/www/html`.	

# Heading1
## Heading2
### Heading3

Press **CTRL+N** then **X** to exit the program.

![Description of the image](/docs/assets/filename.png “Description of the image.”)

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

{{< note >}}
This is a sample note.
{{< /note >}}

{{< caution >}}
This is a sample caution.
{{< /caution >}}
