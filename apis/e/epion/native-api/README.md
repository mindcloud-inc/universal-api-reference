# Epion: Native API Reference

A consolidated summary of Epion's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://epion.nl/integraties
- **API base URL:** `https://api.epion.nl`

## Authentication

### Generic Auth

Generic Epion authentication shell. Runtime Epion API requests require a bearer API token supplied securely at connection time.

### Credentials

- **API Token:** `apiToken` · required · Epion API token generated from Mijn Epion > Integraties. Store this securely in the connection, not in the app definition.

Send these headers with each API request:

```http
Authorization: Bearer <apiToken>
```

[Official authentication documentation](https://epion.nl/integraties)

## API conventions

Responses from this API use JSON. Response data is read from `devices`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Current Measurements](actions/list-current-measurements.md) | `GET /api/current` | [docs](https://epion.nl/integraties) |
