# Project Instalation

**General Requirements**
- Docker
- DockerHub Access Token
- AWS Access Key
- Alchemy API Key
- Pinata API Key

**Organization Secrects**
This secrets are visible for all repositories in this proyect.

```
// Common Org. Secrets
DOCKER_PASSWORD: Your DockerHub Access Token
DOCKER_USERNAME: Your DockerHub username
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
ALCHEMY_API_KEY: API KEY of Alchemy

// Prod Org. Secrets
PROD_CONTRACT_OWNER_SECRET
PROD_PINATA_API_KEY: Pinata API key for Prod
PROD_PINATA_SECRET_API_KEY: Pinata secret for Prod

// Dev Org. Secrets
DEV_CONTRACT_OWNER_SECRET
DEV_PINATA_API_KEY:Pinata API key for Dev
DEV_PINATA_SECRET_API_KEY: Pinata secret for Dev
```

**Create base folder**
```
mkdir sm-marketplace
cd sm-marketplace
```

## Infraestructure

**Requirements**
- Terraform v1.3.4
- AWS account
- NodeJS

_Needs configure AWS Bucket as a Terraform Backend (for generate from scratch see [here](man/new-terraform-backend.md))_

**Up the infraestructure**
```sh
git clone https://github.com/sm-marketplace/infrastructure.git
cd infrastructure
terraform init
terraform plan
terraform apply -auto-approve
terraform output > infra-out
```

Las instacias de EC2 requieren tener docker instalado, para instalar estas dependencias ejecute:

```sh
node scripts/ec2install.js
```

## Web API

SSH_PRIVATE_KEY
DEV_SSH_USER
DEV_SSH_HOST
PROD_SSH_USER
PROD_SSH_HOST

**Requirements**
- 