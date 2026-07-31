# wtfismyip: Native API Reference

A consolidated summary of wtfismyip's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://wtfismyip.com/
- **API base URL:** `https://wtfismyip.com`

## Authentication

### No authentication

wtfismyip public format endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://wtfismyip.com/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Runner IP as Text](actions/get-runner-ip-as-text.md) | `GET /text` | [docs](https://wtfismyip.com/) |
| [Get Runner IP Information](actions/get-runner-ip-information.md) | `GET /json` | [docs](https://wtfismyip.com/) |
| [Get Runner IP Information as XML](actions/get-runner-ip-information-as-xml.md) | `GET /xml` | [docs](https://wtfismyip.com/) |
| [Get Runner IP Information as YAML](actions/get-runner-ip-information-as-yaml.md) | `GET /yaml` | [docs](https://wtfismyip.com/) |
