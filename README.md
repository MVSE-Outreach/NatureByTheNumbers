Nature By The Numbers - Intro To Data Science
=============================================

Setup materials for the June 2015 Digimakers workshop of the same name.

Technical Requirements For Host Machine
---------------------------------------
You should have **VirtualBox**, **Ansible** and **Vagrant** installed.
You will also need to point the vagrant file at an Arch Linux box that matches
the 32/64 bitness of your machine.
Then, running `vagrant up` in the directory will generate a fully provisioned VM.
This vm, by default, will listen to port 8000 on your machine, so point your
attendees that way to access the iPython Jupyter notebook server. The default password
is 'digimakers'. They will need to ignore the security warning, as the certificate is
self signed. It's not worth the hassle to get a proper validated certificate,
but you never know if in the future you might ask people to do a workshop with
data you'd rather not blast out over the wifi for all to see.

If you'd rather not install the provisioners, and would prefer to install things
manually, then please look at the ansible playbook to get a list of the dependencies
for the notebook server setup.

Presentation
------------
The VM is also configured to serve a reveal.js presentation, linked to your machine at port 8001.
To replace this, edit *presentation/* to reflect your new slide deck. All files in the folder are copied
to the root of the presentation serve directory.

Skill Level: Advanced
---------------------
Attendees are expected to understand basic Python. They should know about variables and functions, and should be comfortable with the idea of writing more than one line of Python at a time, rather than using only the interpreter.

Duration of workshop:
---------------------
1 or 2 hours, can be either depending on scheduling requirements.

Details:
--------
The participants will, essentially -

  * Download a dataset about wild bird populations in the UK over time
  * Run some summary statistics on the dataset
  * Make some cool and useful visualisations
  * Get challenged to answer a couple of questions about the data!"

Preparation and Equipment for Attendees:
----------------------------------------
People will need a laptop OR a workstation. If they bring a RPi then that is fine IF there are monitors, keyboards, mice and an internet connection ready to be used, a la the Drop In.
