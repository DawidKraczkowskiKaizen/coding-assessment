# Coding assessment

Your assessment is to design and build a currency exchange tracking application in the AWS lambda environment.

The application should rely on [European Central Bank Data](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html).

Exchange rates should be fetched every day and stored in a database.

Additionally, the application should expose a public REST API endpoint that provides current exchange rate information for all tracked currencies and their change compared to the previous day for all the tracked currencies.

## Business Requirements

- As an API Client, I want to see current exchange rates.
- As an API Client, I want to understand how the exchange rate has changed compared to the previous day.

## Technical Requirements

- The application should be written in python 3.9
- Provided REST endpoint should return data in the JSON format.
  - The application can only use the following AWS Services:
  - AWS Lambda
  - AWS CloudFormation AWS SQS
  - AWS SNS
  - AWS Cloudwatch AWS API Gateway AWS S3
  - AWS DynamoDB AWS Log Insights
- Delivered code and documentation SHOULD follow the best practices
- Application must be fully functioning
- Application must be deployable (either to AWS or localstack )

> You can use cloudformation, CDK, serverless or AWS CLI for the deployment.

# Before you start

- Prepare a new repository of fork this one as a starting point
- Familiarise yourself with existing tooling (poetry, localstack), or use your own with an explanation why you chose it over the proposed one

## Poetry

This repository contains a straightforward poetry setup that you can use to start your work on this assessment. The setup defaults your project name to `ecb`.

To set up the project, you should run:

```shell
poetry install
```

## Localstack

If you are not familiar with localstack, you can use the following shell script to run localstack:

```shell
docker run -v $(PWD)/localstack:/var/lib/localstack --rm -it -p 4566:4566 -p 4510-4559:4510-4559 -d --name localstack localstack/localstack
```

To stop localstack, use the following command:

```shell
docker stop localstack
```

> If you are familiar with `docker-compose`, you can use it instead of the above commands.

# Once you finish

- Make sure to provide the required documentation with an explanation how to run your code
- Contact our HR that you have finished your assessment
- Be prepared to discuss your assessment
