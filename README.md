# pinentry-bash

This utility is `bash` implementation of gpg pinentry program.

The PINEntry is a PIN or passphrase entry dialogs which utilize the Assuan
protocol as specified in the Libassuan manual [1]. You can find the upstream
pinentry collection here [2].

This implementation only uses `bash` and `yad `[3] to display dialogs. But this
implementation can easily be changed to another dialog display program.

Many thanks to Dale Phurrough for the idea. This implementation is inspired by
his pinentry implementation for WSL [4].

1. https://dev.gnupg.org/source/libassuan.git
2. https://dev.gnupg.org/source/pinentry.git
3. https://github.com/v1cont/yad
4. https://github.com/diablodale/pinentry-wsl-ps1

## INSTALL

Configure gpg-agent to use this script for pinentry using one of the following
methods:

1. Set pinentry-program within ~/.gnupg/gpg-agent.conf to the script's path, e.g.
`pinentry-program /path/to/pinentry-bash`

2. Or, set the path to this script when you launch gpg-agent, e.g.
`gpg-agent --pinentry-program /path/to/pinentry-bash`

## LICENSE

Pinentry-bash is licensed under the GNU General Public License version 2.
