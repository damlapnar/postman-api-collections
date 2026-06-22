# Postman API Collections

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-FF6C37?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)

Postman collections for REST API testing with Newman CLI integration. Runs automatically in CI on every push and daily schedule.

## Structure

```
postman-api-collections/
├── collections/
│   └── users-api.json       # Users CRUD test suite
├── environments/
│   └── staging.json         # Staging environment variables
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
