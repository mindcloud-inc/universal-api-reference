# CPSC Recalls Retrieval: Native API Reference

A consolidated summary of CPSC Recalls Retrieval's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en
- **API base URL:** `https://www.saferproducts.gov/RestWebServices`

## Authentication

### No Authentication

The CPSC Recall Retrieval API is publicly available and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Recalls](actions/search-recalls.md) | `GET /Recall` | [docs](https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en) |
