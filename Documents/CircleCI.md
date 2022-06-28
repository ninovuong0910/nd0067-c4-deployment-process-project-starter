# CircleCI
Pipeline will be triggered when there is any code change
Steps:

## Build
1. Setup environment
2. Install dependencies for udagram-frontend
3. Install dependencies for udagram-api
4. Check lint for udagram-frontend
5. Build udagram-frontend
6. Build udagram-api

## Hold
Need approval after build phase to go to deploy phase

## Deploy
1. Setup environment
2. Setup EB
3. Setup AWS-CLI
4. Checkout code
6. Pass secrets from CircleCI to EB
7. Deploy udagram-api 
8. Deploy udagram-frontend