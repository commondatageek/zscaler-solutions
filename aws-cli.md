# AWS CLI

The AWS command line interface needs something special to make it work again.

Copy the zscaler certficate bundle to the `botocore` directory where your AWS CLI tool is installed, and name it `cacert.pem`.

For example:

```
cp zscaler-bundle.pem /usr/local/aws-cli/v2/2.4.11/dist/awscli/botocore/cacert.pem
```

Not sure if it matters, but this assumes that you installed AWS CLI tool using the awscliv2.zip installer, and that you did **NOT** use, for example:

- `pipx`
- `pip`
- `brew`
- or anything else
