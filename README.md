<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Install prerequisites</a></li>
<li><a href="#sec-2">2. Clone gofer</a></li>
<li><a href="#sec-3">3. Build</a></li>
<li><a href="#sec-4">4. Check executable</a></li>
<li><a href="#sec-5">5. Emacs Setup</a>
<ul>
<li><a href="#sec-5-1">5.1. Directory setup</a></li>
<li><a href="#sec-5-2">5.2. Copy contents</a></li>
<li><a href="#sec-5-3">5.3. Init setup</a></li>
<li><a href="#sec-5-4">5.4. Change paths</a></li>
</ul>
</li>
<li><a href="#sec-6">6. Gnu-APL</a>
<ul>
<li><a href="#sec-6-1">6.1. Download and install gnu-apl</a></li>
<li><a href="#sec-6-2">6.2. Install gnu-apl mode for emacs from</a></li>
</ul>
</li>
</ul>
</div>
</div>

# Install prerequisites<a id="sec-1" name="sec-1"></a>

$ sudo apt-get install gcc build-essential git emacs

# Clone gofer<a id="sec-2" name="sec-2"></a>

$ git clone <https://github.com/rusimody/gofer.git>

# Build<a id="sec-3" name="sec-3"></a>

Above should make a directory called gofer [Usually in your home but that depends on where you ran the git clone ]

cd into gofer/src and run

$ make

# Check executable<a id="sec-4" name="sec-4"></a>

Above should make an executable called gofer. When you run it (at shell as:)

$ ./gofer

you should get an error that prelude not found

Set the path thus at shell (make sure the path below is correct!)

$ export PUGOFER=/home/[yourname]/gofer

Now gofer should run (at shell) ie

$ ./gofer

should start

# Emacs Setup<a id="sec-5" name="sec-5"></a>

## Directory setup<a id="sec-5-1" name="sec-5-1"></a>

Make a directory called elisp in ~/.emacs.d

$ cd ~/.emacs.d  
$ mkdir elisp

## Copy contents<a id="sec-5-2" name="sec-5-2"></a>

Copy the files pugofer-init.el and pugofer.el into this elisp directory

## Init setup<a id="sec-5-3" name="sec-5-3"></a>

Add this line to end of ~/.emacs.d/init.el

(add-to-list 'load-path (expand-file-name "~/.emacs.d/elisp"))

## Change paths<a id="sec-5-4" name="sec-5-4"></a>

Look for setenvs in pugofer-init.el
Change these to your paths
Copy this whole file to bottom of ~/.emacs.d/init.el

# Gnu-APL<a id="sec-6" name="sec-6"></a>

## Download and install gnu-apl<a id="sec-6-1" name="sec-6-1"></a>

Download deb from <https://www.gnu.org/software/apl/>  [Rpm if Fedora]
Install using sudo dpkg -i [filename]

## Install gnu-apl mode for emacs from<a id="sec-6-2" name="sec-6-2"></a>

<https://github.com/lokedhs/gnu-apl-mode>