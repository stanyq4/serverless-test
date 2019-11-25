# serverless-test
> <b>serverless</b>

An awesome project to run Desktop API tests in serverless environment

## Installing / Getting started

#### Serverless Setup
When working with a serverless project for the first time, some setup is required.
- Download AWS CLI https://aws.amazon.com/cli/
- Create CLI IAM user with Programmatic access, but NOT AWS Management Console access. If you do not have access to do this yourself, ask DevOps
-- Choose Q4Admin-CLI for group
-- Copy key and secret returned in the last step
- Install AWS CLI locally
- Run aws configure
-- Enter the access key, secret key and region when prompted.  Region is us-east-1

#### NPM and Node setup
 - Download and Install LTS Node version from https://nodejs.org/en/download/
 
#### Serverless cli setup

```shell
npm install -g serverless
```

## Developing

Download the repo and install npm dependencies

```shell
git clone https://github.com/stanyq4/serverless-test.git
cd serverless-test/
npm install
```

Invoke function locally

```shell
serverless invoke local --function testFunc
```

### Initial Configuration

Required environment variables 

#### MONGODB_URI
Type: `String`  
Default: `'mongodb://localhost/q4app'`

### Deploying / Publishing

Deploy your function to aws environement 

```shell
serverless deploy --function testFunc --stage dev
```

Your function will be available via API Gateway:
- API Gateway: GET https://m14kkupz623139.execute-api.us-east-1.amazonaws.com/dev/testFunc

## Links

- Issue tracker: https://q4websystems.atlassian.net/secure/RapidBoard.jspa?rapidView=171
- Related projects:
  - Factset: https://github.com/q4mobile/serverless-factset
