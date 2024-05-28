
# Coding Assessment

Your task is to design and build a currency exchange tracking application using the AWS Lambda environment.

The application should source data from the [European Central Bank Data](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html).

Exchange rates should be fetched daily and stored in a database.

Additionally, the application should provide a public REST API endpoint that offers current exchange rate information for all tracked currencies and their day-to-day changes.

## Business Requirements

- As an API Client, I want to view current exchange rates.
- As an API Client, I want to understand how the exchange rate has changed compared to the previous day.

## Technical Requirements

- The application must be written in Python 3.10 or greater.
- The provided REST endpoint should return data in JSON format.
- Only the following AWS Services are permitted:
  - AWS Lambda
  - AWS CloudFormation
  - AWS SQS
  - AWS SNS
  - AWS CloudWatch
  - AWS API Gateway
  - AWS S3
  - AWS DynamoDB
  - AWS Log Insights
- The delivered code and documentation **SHOULD** adhere to best practices.
- The application must be fully functional and deployable (either to AWS or localstack).

> Deployment can be managed via CloudFormation, CDK, Serverless, or AWS CLI.

# Before You Start

- Prepare a new repository or fork this one as a starting point.
- Familiarise yourself with the existing tooling (Poetry, Localstack), or explain your choice of alternative tools.

## Poetry

This repository includes a basic Poetry setup named `ecb`.

To initialize the project, run:

```shell
poetry install
```

## Localstack

For those unfamiliar with Localstack, the following shell script can be used to run it:

```shell
docker run -v $(PWD)/localstack:/var/lib/localstack --rm -it -p 4566:4566 -p 4510-4559:4510-4559 -d --name localstack localstack/localstack
```

To stop Localstack, execute:

```shell
docker stop localstack
```

> If you are comfortable with `docker-compose`, feel free to use it instead.

# Completion

- Ensure all required documentation is provided, explaining how to execute your code.
- Notify our HR department upon completion of your assessment.
- Be prepared to discuss your project.
