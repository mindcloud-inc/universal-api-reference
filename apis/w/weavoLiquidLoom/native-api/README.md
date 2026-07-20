# Weavo Liquid Loom: Native API Reference

A consolidated summary of Weavo Liquid Loom's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/weavoliquidloom/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/Weavo%20Liquid%20Loom/apiDefinition.swagger.json
- **API base URL:** `https://liquidloom.weavo.no`

## Authentication

### API Key

Authenticate requests with a Weavo Liquid Loom API key in the ApiKey header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#creating-a-connection)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [CSV to JSON](actions/csv-to-json.md) | `POST /api/CsvToJson` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#csv-to-json) |
| [CSV to Text](actions/csv-to-text.md) | `POST /api/CsvToText` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#csv-to-text) |
| [CSV to XML](actions/csv-to-xml.md) | `POST /api/CsvToXml` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#csv-to-xml) |
| [JSON to JSON](actions/json-to-json.md) | `POST /api/JsonToJson` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#json-to-json) |
| [JSON to Text](actions/json-to-text.md) | `POST /api/JsonToText` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#json-to-text) |
| [JSON to XML](actions/json-to-xml.md) | `POST /api/JsonToXml` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#json-to-xml) |
| [XML to JSON](actions/xml-to-json.md) | `POST /api/XmlToJson` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#xml-to-json) |
| [XML to Text](actions/xml-to-text.md) | `POST /api/XmlToText` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#xml-to-text) |
| [XML to XML](actions/xml-to-xml.md) | `POST /api/XmlToXml` | [docs](https://learn.microsoft.com/en-us/connectors/weavoliquidloom/#xml-to-xml) |
