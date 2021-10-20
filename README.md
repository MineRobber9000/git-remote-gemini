# git-remote-gemini

currently does not work, but just needs a fetch implementation and it should work.

## how to use

when the fetch implementation is added you can put `git-remote-gemini` in your PATH and it should allow you to clone via gemini.

the TOFU database is stored at `$XDG_CONFIG_HOME/tofu.db`. if you get a TOFU error when attempting to clone a repository, verify the certificate fingerprint out of band and then supply the environment variable `REMOTE_GEMINI_TRUST=1`. git-remote-gemini will add the new certificate fingerprint to the trust database.

if asn1crypto is available, git-remote-gemini will use it to store the fingerprint of the cert's public key, rather than the cert itself. the fingerprint provided for verification will always be of the cert itself, however.

push via gemini is not available and will not be, the reasons for which should be obvious to anybody who knows gemini.
