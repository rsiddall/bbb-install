# bbb-install

Install BigBlueButton 1.0 using the instructions at http://docs.bigbluebutton.org/install/install.html, and optionally install the development environment and tools.

This is an interactive installation.  You cannot leave it unattended as you will need to confirm installation of some items and agree to licenses.

The installation process changes for each major release of BBB, so these scripts will require updating for BBB 1.1.

	bbb-install [-h] [-c] [-m extra-modules] [-p ffmpeg-ppa-url] [-n hostname-or-ip] [-s tls_hostname]
	where:
		-c = Do not enable SSL
		-h = Help
		-m = Extra BBB modules to install, e.g. -m 'bbb-demo bbb-check'
		-p = PPA to use to install ffmpeg, e.g. -p mc3man/trusty-media
		-n = BBB hostname or IP address (if not default)
		-s = SSL hostname to use in configuration, if not default hostname

The script will try to install ffmpeg from source, as specified in the BBB installation instructions, if no PPA is supplied.  This is far slower than using a PPA.

The SSL certificate, key, and intermediate CA must be in ssl.crt, ssl.key, and ssl.ca in the same folder as the script.

