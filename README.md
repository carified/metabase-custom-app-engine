# metabase-custom-app-engine
Configuration files for deploying metabase to GCP app engine


## Requirements

* `gcloud` command line tool available at https://cloud.google.com/sdk/install


## Deployment

1) `cp .env.example .env` and make sure proper secrets are set
2) generate app file `source .env && eval "cat <<< \"$(<app.yml.example)\"" 2> /dev/null > app.yml`
3) `gcloud app deploy app.yml`
