# zscaler-solutions

When my company started using Zscaler, everything broke.  Especially if Docker is part of your daily workflow.

Here are some ideas for making things work with Zscaler again.

Work in progress.


## Broken Things

- stuff on my local mac
- almost all docker containers
- common utilities
  - curl
  - wget
  - AWS CLI tool
  - python
  - boto3
    - environment variables
      - CA_BUNDLE
      - AWS_CA_BUNDLE
    - `verify` parameter on client construction
  - anything that uses the OS certificate store
