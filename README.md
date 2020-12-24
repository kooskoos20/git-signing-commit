###Signing commits on github

####Configure your name and email on github
```
git config user.name "<your-name>"
git config user.email "<your-email>"
```

####Generating GPG key to sign commits

```
gpg --full-generate-key
```

####Confirm key was added
```
gpg --list-secret-keys --keyid-format LONG
```

####Export key to add to GPG keys on github in your profile

```
gpg --export --armor <KEY-ID> //Can be found next to sec rsa4096/<KEY-ID> in the list secret keys output
```

####Cofigure github to use this key sign your commits

```
git config --global user.signingkey <KEY-ID>
```

####Configure github to sign all commits, use -S flag to sign individual commits instead

```
git config --global commit.gpgsign true
```
