# Contributing to postman-api-collections

Thank you for your interest in contributing!

## Getting Started

```bash
git clone https://github.com/damlapnar/postman-api-collections.git
cd postman-api-collections
npm install -g newman newman-reporter-htmlextra
```

## Running Tests

```bash
newman run collections/users-api.json --environment environments/staging.json
```

## Guidelines

- Follow the existing code style and naming conventions
- Add tests for any new functionality
- Keep commits small and focused with descriptive messages
- Open an issue before submitting large changes

## Pull Request Process

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/your-feature`)
3. Commit your changes with a descriptive message
4. Push to your fork and open a Pull Request against `main`
5. Ensure all CI checks pass

## Reporting Bugs

Open a GitHub Issue with:
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, browser/runtime version)
