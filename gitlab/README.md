# Gitlab Pipeline

Everything is managed in a separate repo over on Gitlab (fly -t tutorial trigger-job -w -j hello-ci/deploy-app). 

However, the file `.gitlab-ci.yml` is the pipeline used for gitlab-ci. This file is in the root directory of the repo in Gitlab. When Gitlab sees this file, it reads it and builds a pipeline from it. Credentials for pushing to Cloud Foundry are provided via Environment Variables configured in the Gitlab repo.
