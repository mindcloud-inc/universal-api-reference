# Mime Automation: Native API Reference

A consolidated summary of Mime Automation's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/mimeautomationip/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/independent-publisher-connectors/Mime%20Automation/apiDefinition.swagger.json
- **API base URL:** `https://accloudsolutions.p.nadles.com`

## Authentication

### API Key

Use an API key for the Mime Automation API. The runtime sends it as the X-Billing-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Billing-Token: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/mimeautomationip/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Files From EML](actions/extract-files-from-eml.md) | `POST /MimeAutomation/ExtractFilesFromEml` | [docs](https://learn.microsoft.com/en-us/connectors/mimeautomationip/#extract-files-from-a-base64-encoded-eml-file) |
| [Extract Files From TNEF](actions/extract-files-from-tnef.md) | `POST /MimeAutomation/ExtractFiles` | [docs](https://learn.microsoft.com/en-us/connectors/mimeautomationip/#extract-files-from-a-tnef-encoded-file) |
