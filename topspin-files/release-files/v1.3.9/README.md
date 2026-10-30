# Introduction

These are the instructions for getting and installing the TopSpin
version of Opto. If you are looking for the OVJ version please
go here: [README-OVJ.md](https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/ovj-files/README-OVJ.md)

# System Requirements
  
    Software
    
    - A computer running an OS that will run TopSpin 3.6.x or later
    
        Read about TopSpin HERE:
        
          https://www.bruker.com/en/products-and-solutions/mr/nmr-software/topspin.html
      
        That site says supported OSes include:
        
          AlmaLinux 9.2
          CentOS 7
          Windows 10
          Windows 11.
          
        We have tested on:
        
          AlmaLinux 9.X
          CentOS 7

        Note that Opto Topspin does not yet support Windows
            
    - An installation of TopSpin 3.6.x or later
    
        To learn how to install TopSpin please visit the Bruker website
      
          https://www.bruker.com

        We have tested on:
      
          TopSpin 3.6.X
          TopSpin 4.3.0
          TopSpin 4.4.x
        
        It is possible it will work with other as yet untested versions
          of TopSpin.
      
      
      - An installation of java on your computer
      
          OPTO needs a Java JDK (like OpenJDK) installed on your system.
          
          Install via: sudo apt install openjdk-<YOUR_DESIRED_VERSION>-jdk
          
          YOUR_DESIRED_VERSION could be 8, 11, 17, or 21. Most testing has taken
          place on 11.
          
          Warning a JDK is required. Not a JRE. And certainly not a headless
          JRE. If apt reports your installed java as jre-headless you will
          need to install some other version of java.

    Hardware

    - A Bruker spectrometer / magnet combo
      
        Attached to the host computer

# Download components

Application Install Package
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/topspin-files/release-files/v1.3.9/opto-topspin.zip
    
Manual
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/topspin-files/release-files/v1.3.9/opto-help.pdf
    
Insider's Guide

  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/topspin-files/release-files/v1.3.9/InsidersGuideToOPTO.pdf
    
Example Job
    
  https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/topspin-files/release-files/v1.3.9/example.zip
  
# Installation guide

    Total time spent installing will be a few minutes
    
    Copy the already donwloaded opto-topspin.zip installer package into
      your home directory as ~/opto-topspin.zip
      
    Extract it under your home directory
    
      mkdir ~/opto-tmp
      cd ~/opto-tmp
      unzip ../opto-topspin.zip
     
    run the install program
     
      sudo ./install.sh <topspin version>
      
      (You will be asked for a password. The Opto install process requires
       sudo access by the logged in user to the machine in order to work.)
      
      <topspin version> can be names like topspin3.6.5 etc.
      It is the name of the installation directory under /opt
      where the versions of TopSpin reside.

    At this point the opto.sh executable script and supporting installation
    files are installed in /opt/<topspin version>
    
    You can delete the ~/opto-tmp directory and all its contents

# Uninstall guide

  If Opto has already been installed there is an uninstall-opto.sh
  executable script in the path. Simply run
  'sudo uninstall-opto.sh \<topspin version\>' and Opto files will be
  removed from the installation directories. Your Opto job files and
  setting files will remain.
    
# Instructions for use
  
    Launch TopSpin
    
    Run the command open-opto.py from within TopSpin

      TopSpin will start listening and will launch the Opto GUI
    
    The Opto gui allows one to build jobs and run them

    In the Opto gui define your job and the press the Run button
   
      To learn about jobs and how to build then read the already downloaded manual.
      
    The terminal window will show output progress from the
      running Opto job.
    
    When running an optimization log files are written to the current
      experiment directory with names starting with "OPTO-*". These can
      be useful for figure creation and for checking the accuracy of the
      results.

# Project site

  The public facing OPTO project page is [HERE](https://git.doit.wisc.edu/nmrfam-public/opto-releases/-/blob/main/README.md)
  
  Go there to read more about the Opto project on all platforms, etc.

# LICENSE

  OPTO® TOPSPIN Copyright © 2024 created by Barry Dezonia et al, University of
  Wisconsin-Madison NMRFAM. All Rights Reserved by the Wisconsin Alumni
  Research Foundation. All rights reserved.

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
