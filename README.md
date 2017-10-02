# Bash Completions For Coverity

Suggests arguments and options for various Coverity commands.

# Installation

In all cases, you simply need to install the appropriate bash
completion package (if not already installed) and then copy
the `coverity` completion script from this repository into the right directory. For example:

```bash
sudo apt-get install bash-completion
curl -sL https://raw.githubusercontent.com/thaljef/Coverity-Bash-Completion/master/coverity > /etc/bash_completion.d/coverity
bash -l; # To start new shell
```

# Usage

For this completions to work, the `bin` directory for the Coverity Platform
and/or Coverity Analysis Tools must be in your `$PATH`.

At this time, completions are available only for some commands.  Here are
some of my favorites:

```bash
$> cov-admin-db [TAB][TAB]

backup          optimize        reset-admin-db  restore
```

```bash
$> cov-configure --delete-compiler-config temp[TAB][TAB]

template-apt-config-0             template-gcc-config-3
template-g++-config-0             template-gcc-config-4
template-g++-config-1             template-gcc-config-5
template-g++-config-2             template-javac-config-0
template-g++-config-3             template-java-config-0
```

```bash
$> cov-configure --comptype iar[TAB][TAB]

iar:430        iar:hcs12      iar:sam8       iar_cxx:avr32  iar_cxx:rh850
iar:8051       iar:m16c       iar:sh         iar_cxx:cr16c  iar_cxx:rl78
iar:arm        iar:m32c       iar:v850       iar_cxx:h8     iar_cxx:sh
iar:avr        iar:maxq       iar_cxx:430    iar_cxx:hcs12  iar_cxx:v850
```

```bash
$> cov-analyze --enable BAD[TAB][TAB]

BAD_ALLOC_ARITHMETIC    BAD_COMPARE             BAD_LOCK_OBJECT
BAD_ALLOC_STRLEN        BAD_EQ                  BAD_OVERRIDE
BAD_CERT_VERIFICATION   BAD_EQ_TYPES            BAD_SHIFT
BAD_CHECK_OF_WAIT_COND  BAD_FREE                BAD_SIZEOF
```

# Author

Jeffrey Ryan Thalhammer <jeff@thaljef.org>

# Copyright

2017 (C) Synopsys, Inc.