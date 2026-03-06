# aws-barbershop-booking

Serverless appointment booking system for hair salons built on AWS.

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
| Lambda | Business logic (Python or Node.js) |
| DynamoDB | Appointment storage |
| SES | Email confirmations |
| IAM | Roles and permissions |

## Infrastructure

AWS SAM is the recommended tool for this project.

Alternatives:
- **Serverless Framework** — minimal boilerplate
- **Terraform** — more verbose but more complete

## Cost Estimate

< USD 0.50/month for a small barbershop (~1,500 appointments/month), excluding free tier.

## Project Structure (planned)

```
aws-barbershop-booking/
├── AGENTS.md
├── README.md
├── LICENSE
├── template.yaml          # AWS SAM template
├── frontend/              # Static S3 site
│   ├── index.html
│   ├── style.css
│   └── app.js
└── functions/             # Lambda functions
    ├── create-booking/
    ├── get-bookings/
    └── cancel-booking/
```

## Key Decisions

- Language: TBD (Python or Node.js for Lambda)
- Infrastructure tool: AWS SAM
- Database: DynamoDB (single-table design preferred)
- Auth: TBD
