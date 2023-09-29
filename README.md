# himan-chart

Helm chart for Himan

source: https://github.com/fmidev/himan.git

# Contents

Chart contains configuration for Himan openshift job template.

# Preconditions

Necessary passwords and accounts need to be created before creating the chart.

radon-credentials are given with secret radon-credentials (configurable), secret should contain following fields:

* RADON_HOSTNAME
* RADON_PORT (optional, default: 5432)
* RADON_DATABASENAME (optional default: radon)
* RADON_WETODB_PASSWORD

s3-credentials are given with secret s3-credentials (configurable), secret shouldcontain following fields

* S3_ACCESS_KEY_ID
* S3_SECRET_ACCESS_KEY

If no credentials are needed for s3 access, leave name field empty.

# Usage

helm create himan .

Nearly all of the options of Himan are exposed to the job template. See the template for more details.
