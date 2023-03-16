# [kacyluker.github.io](https://kacy-luker.github.io/kacyluker.github.io/)
## Master Instructions
This repo contains the various versions of my personal portfolio website. I use the release branches to toggle which site I wish to deploy.

### Setup for Custom Domain Name
#### 1) Github Settings
1. Under `Pages` set `Custom domain` to `KacyLuker.com`

#### 2) Create a CNAME record
1. Navigate to [DNS provider](https://www.dynu.com)
2. Create a CNAME recorde that points to `https://kacy-luker.github.io/kacyluker.github.io/`

#### 3) Confirm Recode Configured Correctly
In Git Base use the following command
```console
$ dig www.KacyLuker.com +nostats +nocomments +nocmd
```
The following is an example of expected output:
```console
    > www.KacyLuker.com.                    IN      A
    > www.KacyLuker.com.            3592    IN      CNAME   kacyluker.github.io.
    > YOUR-USERNAME.github.io.      43192   IN      CNAME   GITHUB-PAGES-SERVER .
    > GITHUB-PAGES-SERVER .         22      IN      A       192.0.2.1
```
