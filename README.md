SCRAMBLE(1) - General Commands Manual

# NAME

**scramble** - scrambles text with different substitution schemes

# SYNOPSIS

**scramble**
\[**-c**&nbsp;*code*]
\[**-d**]
\[**-n**&nbsp;*number*]
\[**-v**]
\[*text*]  
**scramble**
\[**-h**]

# DESCRIPTION

**scramble**
scrambles text with different substitution alphabeths.
By default, it reads applies ROT-13 "encryption" to
stdio(3).

The following options are available:

**-c** *code*

> Use monoalphabetic substitution with keyword (caesar with codeword).

> If the codword comprises all 26 characters of the alphabet, of course this
> will become a generic monoalphabetic substitution cipher.

**-d**

> Backwards-encrypt (decrypt).

\[n *number*]

> Apply Caesar cipher with rotation of
> *number*
> characters (ROT-n).
> \[**-v**]
> Verbose output.
> \[*text*]
> Scramble
> *text*
> instead of standard input.

# EXIT STATUS

The **scramble** utility exits&#160;0 on success, and&#160;&gt;0 if an error occurs.

# EXAMPLES

Scramble a sentence with ROT-13

	$ echo The quick brown fox jumps over the lazy dog | scramble

Scramble a sentence with monoalphabetic substitution with codeword "CAESAR"

	$ echo The quick brown fox jumps over the lazy dog | scramble -c CAESAR

Unscramble the same sentence:

	$ echo Tfr ougei apmwl bmx huknq mvrp tfr jczy smd | scramble -c CAESAR -u

# HISTORY

The
**scramble**
utility has been available since 2018.

# AUTHORS

David Dahlberg &lt;[dyn+code@dahlberg.cologne](mailto:dyn+code@dahlberg.cologne)&gt;

Debian - May 7, 2018
