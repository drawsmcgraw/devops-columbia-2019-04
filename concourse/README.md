# Concourse Artifacts

### Setting the Pipeline in Concourse
```
# Login to a local Concourse, creating the alias 'tutorial'.
fly --target tutorial login --concourse-url http://127.0.0.1:8080 -u admin -p admin

# Set the pipeline, loading creds from the file 'credentials.yml'
fly -t tutorial set-pipeline \
  -p hello-ci \
  -c pipeline.yml \
  -l credentials.yml

# Trigger the pipeline, watching the output
fly -t tutorial trigger-job \
  -w \
  -j hello-ci/deploy-app
```
