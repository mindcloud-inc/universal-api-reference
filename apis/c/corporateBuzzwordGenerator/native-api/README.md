# Corporate Buzzword Generator: Native API Reference

A consolidated summary of Corporate Buzzword Generator's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://github.com/sameerkumar18/corporate-bs-generator-api
- **API base URL:** `https://corporatebs-generator.sameerkumar.website`

## Authentication

### No authentication

Public endpoint with no credentials required.

This API does not require request authentication.

[Official authentication documentation](https://github.com/sameerkumar18/corporate-bs-generator-api)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Corporate Buzzword](actions/generate-corporate-buzzword.md) | `GET /` | [docs](https://github.com/sameerkumar18/corporate-bs-generator-api) |
