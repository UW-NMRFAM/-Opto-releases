# Introduction

These are the instructions for getting and installing the OVJ
version of OPTO. If you are looking for the TopSpin version
please go here: [README-TOPSPIN.md](https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/topspin-files/README-TOPSPIN.md)

# System requirements
  
    Software
    
    - A computer running an OS that will run OpenVNMRJ (newer than 3.1A)
    
        The OpenVNMRJ project is here: https://github.com/OpenVnmrJ/OpenVnmrJ
      
        The project README for 3.2A says supported OSes include:
        
          AlmaLinux: Version 8 and 9.
          RHEL: Version 8 and 9.
          Ubuntu: Version 20, 22, and 24.
        
        We have tested on:
        
          Ubuntu 20.04

    - An installation of OVJ newer than 3.1A
    
        To learn how to install OVJ see https://github.com/OpenVnmrJ/OpenVnmrJ/releases
      
        We have tested on:
      
          OVJ 3.1A with custom code changes in vnmrsys

            (The current master branch of OVJ already includes our custom code changes)

          OVJ 3.2A

            (OVJ 3.2A already contains our custom code changes as well)
        
        It is possible it will work with old Agilent versions
          of VNMRJ but they have not yet been tested.
      
      - An installation of java on your computer
      
          OPTO needs a Java JDK (like OpenJDK) installed on your system.
          
          Install via: sudo apt install openjdk-<YOUR_DESIRED_VERSION>-jdk
          
          YOUR_DESIRED_VERSION could be 8, 11, 17, or 21. Most testing has taken
          place on 11.
          
          Warning a JDK is required. Not a JRE. And certainly not a headless
          JRE. If apt reports your installed java as jre-headless you will
          need to install some other version of java.

    Hardware

    - A Varian (Agilent) spectrometer / magnet combo
      
        Attached to the host computer

# Download components

Application Install Package
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/ovj-files/release-files/v1.3.9/opto-ovj.zip
    
Manual
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/ovj-files/release-files/v1.3.9/opto-help.pdf
    
Insider's Guide

  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/ovj-files/release-files/v1.3.9/InsidersGuideToOPTO.pdf
    
Example Job
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/ovj-files/release-files/v1.3.9/example-data.zip
    
# Installation guide

    Total time spent installing will be a few minutes
    
    Extract the downloaded opto-ovj.zip into your home directory
    
      mkdir ~/opto-tmp
      cd ~/opto-tmp
      unzip ../opto-ovj.zip
     
    run the install program
     
      sudo ./install.sh
      
      (You will be asked for a password. The OPTO install process requires
       sudo access by the logged in user to the machine in order to work.)

    At this point the opto.sh executable script and supporting installation
    files are installed in /vnmr/bin
    
    You can delete the ~/opto-tmp directory and all its contents
    
# Uninstall guide

  If OPTO has already been installed there is an uninstall-opto.sh
  executable script in the path. Simply run 'sudo uninstall-opto.sh' and
  OPTO files will be removed from the installation directories. Your OPTO
  job files and setting files will remain.
      
# Instructions for use
  
  Refer to the OPTO manual as downladed earlier as needed.
  
  Launch OpenVnmrJ
  
  In the command entry field inside OVJ type "listenon"
  
  From a terminal run opto.sh (it is already in your path)
  
  Opto will launch and start communicating with OVJ
    
    The Opto gui allows one to build jobs and run them

    In the Opto gui define your job and the press the Run button
   
      To learn about jobs and how to build them read the manual you
      downloaded earlier.
          
    The terminal window will show output progress from the
      running Opto job.
    
    When running an optimization log files are written to the current
      experiment directory with names starting with "OPTO-*". These can
      be useful for figure creation and for checking the accuracy of the
      results.

# Project site

  The public facing OPTO project page is [HERE](https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/README.md)
  
  Go there to read more about the OPTO project on all platforms, etc.

# LICENSE

  OPTO® OVJ Copyright © 2024 created by Barry Dezonia et al, University of
  Wisconsin-Madison NMRFAM. All Rights Reserved by the Wisconsin Alumni
  Research Foundation.

  The Regents of the University of Wisconsin-Madison hereby grant the end
  user an internal, non-exclusive, non-commercial license to NMRFAM software
  for academic and scholarly purposes only. The end user agrees and
  acknowledges that redistribution to third parties not covered by this
  license is explicitly prohibited.

  THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
  AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
  IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
  ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
  LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
  CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
  SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
  INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
  CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
  ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
  POSSIBILITY OF SUCH DAMAGE.

  For non-academic use, please contact Justin Anderson at the Wisconsin
  Alumni Research Foundation (janderson@warf.org) to obtain a commercial
  license.
  
# How to cite

  Citation: All publications resulting from the use of this software should cite the following paper:
  
  OPTO: Automated Optimization for Solid-State NMR Spectroscopy, Collin G. Borcik, Barry
  DeZonia, Thirupathi Ravula, Benjamin D. Harding, Rajat Garg, and Chad M. Rienstra Journal of the
  American Chemical Society 2025 147 (4), 3293-3303 DOI: 10.1021/jacs.4c13295

  [Article link](https://pubs.acs.org/doi/full/10.1021/jacs.4c13295) 
