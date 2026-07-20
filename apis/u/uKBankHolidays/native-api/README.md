# UK Bank Holidays: Native API Reference

A consolidated summary of UK Bank Holidays's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.api.gov.uk/gds/bank-holidays/
- **API base URL:** `https://www.gov.uk`

## Authentication

### No authentication

The GOV.UK Bank Holidays API is a public JSON endpoint and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.api.gov.uk/gds/bank-holidays/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Bank Holidays](actions/list-bank-holidays.md) | `GET /bank-holidays.json` | [docs](https://www.api.gov.uk/gds/bank-holidays/) |
