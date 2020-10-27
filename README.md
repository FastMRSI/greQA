# greQA
SNR measurements (in each channel and for combined image), for a GRE acquisition
Linux Installation:

If files needed and Matlab Runtime are installed within a user’s home directory, no root/superuser permissions should be required. Local installation packages (which include the Matlab Runtime) are located at  https://pitt.box.com/s/sedtq105ehmve7ni8cd5ty8h7zjk5pwp 

-Open a terminal and go (cd) to the directory which has the installation package
> ./greSNR_localInstaller.install &
-Follow directions (the default installation directories require root).

Add an alias to your .bashrc file (use your favorite editor or, as follows, replacing the path/username here with your installation directory):
> cd ~   								# switch to your home directory
> cp .bashrc .bashrc_org            					# make a copy of the .bashrc file
> echo “alias greSNR='/usr/greSNR/application/run_greSNR.sh /usr/local/MATLAB/MATLAB_Runtime/v99'” >> .bashrc   	# add alias to .bashrc file

(Note: Use >>, to append the .bashrc file, rather than just >, which would create a new .bashrc file with just the alias line)
-Open a new terminal window, to make use of your newly edited .bashrc file


Help:

> greSNR -help

Usage:

> greSNR &

OR 

> greSNR twixGREfile savePicsTrueFalse &

-twixGREfile is the GRE raw/twix data file from the scanner scanner. Use relative or absolute path if not in CWD

-savePicsTrueFalse: To generate pics, enter 1 (if 2nd argument not present, this is the default). If no connection to the X server, enter 0 here.
