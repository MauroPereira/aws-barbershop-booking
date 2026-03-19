# aws-hairsalon-booking

**Autor**: Mauro A. Pereira
**Email**: mauro.a.pereira@gmail.com

## Description

Serverless appointment booking system for hair salons built on AWS. Allows customers to book, view, and cancel appointments through a static web frontend backed by AWS Lambda, API Gateway, and DynamoDB.

## Architecture

```
User → S3 (static frontend) → API Gateway → Lambda → DynamoDB
                                                     → SES (email confirmation)
```

## AWS Services

| Service | Role |
|---|---|
| S3 | Static frontend hosting |
| API Gateway | HTTP entry point |
| Lambda | Business logic |
| DynamoDB | Appointment storage |
| SES | Email confirmations |
| IAM | Roles and permissions |

## Infrastructure

Managed with **AWS SAM** (`template.yaml`).

## Current version

`0.1.0-dev`

## Changelog

- `0.1.0-dev` - 2026-03-19: Initial project setup and documentation
