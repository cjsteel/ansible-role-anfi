
ansible-role-afni
=================

An Ansible role to install and manage **ANFI** (Analysis of Functional NeuroImages)


Description
-----------

**AFNI** is a set of C programs for processing, analyzing, and displaying functional MRI (FMRI) data - a technique for mapping human brain activity. It runs on Unix+X11+Motif systems, including SGI, Solaris, Linux, and Mac OS X. It is available free (in C source code format, and some precompiled binaries) for research purposes.

## Notes

- By default, most AFNI command line instructions assume that tcsh is the chosen shell for a terminal. Also, many Message Board postings and scripts in demos, which may be useful for reference, are written in tcsh. So, the choice is yours, but choose wisely...
- Can probably be installed by users to home directories
- Ansible installer could add acemenu entry.

Resources
---------

* [ ANFI Home ](https://afni.nimh.nih.gov/afni )
* [ afni github project]( https://github.com/afni/afni )
* [ Installation overview ]( https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/overview.html )
* [ Ubuntu Linux Installation] ( https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/steps_linux_ubuntu.html#install-steps-linux-ubuntu )



Requirements
------------




Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

### roles/afni/defaults/main.yml

```yaml
---
# file: roles/afni/defaults/main.yml

# shell

afni_shell: 'tcsh' # 'bash'...
afni_shell_path: chsh -s /bin/{{ afni_shell }}

# package

afni_arch : 'amd64'
afni_ver  : '1.0.2-2'
afni_pkg  : 'libxp6_{{ afni_ver }}_{{ afni_arch }}.deb'
afni_deb_url  : 'http://mirrors.kernel.org/ubuntu/pool/main/libx/libxp/{{ afni_pkg }}'

# 

```




Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: cjsteel.ansible-role-afni, x: 42 }


License
-------

BSD


Author Information
------------------

Christopher Steel
Systems Administrator
McGill Centre for Integrative Neuroscience
Montreal Neurological Institute
McGill University
3801 University Street
Montréal, QC, Canada H3A 2B4
Tel. No. +1 514 398-2494
E-mail: christopherDOTsteel@mcgill.ca
[MCIN](http://mcin-cnim.ca/), [theneuro.ca](http://theneuro.ca)
