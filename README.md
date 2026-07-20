# Postman API Collections

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-FF6C37?style=flat-square)
[![CI](https://github.com/damlapnar/postman-api-collections/actions/workflows/newman.yml/badge.svg)](https://github.com/damlapnar/postman-api-collections/actions/workflows/newman.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Postman collections for REST API testing with Newman CLI integration. Runs automatically in CI on every push and daily schedule.

## Structure

```
postman-api-collections/
├── collections/
│   └── users-api.json       # Users CRUD test suite
├── environments/
│   ├── staging.json         # Staging environment variables
│   └── production.json      # Production environment variables
└── .github/workflows/
    └── newman.yml           # CI pipeline
```

## Running Locally

```bash
npm install -g newman newman-reporter-htmlextra

newman run collections/users-api.json \
  --environment environments/staging.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export reports/report.html
```
