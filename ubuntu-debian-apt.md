# Debian/Ubuntu `apt` with PPAs

"PPAs are for non standard software/updates. They are generally used by people who want the latest and greatest."[^1]

I was building a docker container and wanted to get the latest version of Ansible (instead of the 2.10 that was available via standard `apt` channels).

```
# Get Zscaler added to certificate store
RUN apt-get -y install ca-certificates
ADD zscaler.crt /usr/local/share/ca-certificates
RUN update-ca-certificates

# Get the PPA for Ansible and install
RUN apt-get -y install software-properties-common
RUN apt-add-repository -y ppa:ansible/ansible       # This was the line that was failing due to SSL cert validation
RUN apt-get -y install ansible
```

[^1]: https://askubuntu.com/questions/4983/what-are-ppas-and-how-do-i-use-them
