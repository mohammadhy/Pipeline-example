How Have Code Signing
- gpg --full-generate-key
- gpg --armor --export <Your-Key-ID>
- git config --global user.signingkey <Your-Key-ID>
- git config --global commit.gpgsign true
