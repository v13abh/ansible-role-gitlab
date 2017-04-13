# OULibraries.gitlab

This role installs [GitLab Community Edition (CE)](https://gitlab.com/gitlab-org/gitlab-ce) on Centos7. Complete GitLab documentation can be found at https://docs.gitlab.com/ce/.

## Dependencies

* [OU Libraries Centos7 Role](https://github.com/OULibraries/ansible-role-centos7)
* [OU Libraries Users Role](https://github.com/OULibraries/ansible-role-users)

## Hardware Requirements

Taken from the [official documentation](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/install/requirements.md#hardware-requirements):

### CPU

  * 1 core supports up to 100 users but the application can be a bit slower due to having all workers and background jobs running on the same core
  * 2 cores is the recommended number of cores and supports up to 500 users

### Memory

You need at least 4GB of addressable memory (RAM + swap) to install and use GitLab! The operating system and any other running applications will also be using memory so keep in mind that you need at least 4GB available before running GitLab. With less memory GitLab will give strange errors during the reconfigure run and 500 errors during usage.

  * 1GB RAM + 3GB of swap is the absolute minimum but we strongly advise against this amount of memory. See the unicorn worker section below for more advice.
  * 2GB RAM + 2GB swap supports up to 100 users but it will be very slow
  * 4GB RAM is the recommended memory size for all installations and supports up to 100 users

## Initial Configuration

After installation, direct your browser to the URL configured in defaults\main.yml. You will be prompted to change the password for the Root account.
