# <img src="https://images.mindcloud.co/apps/icons/weavo-app-icon_1777580253823.png" alt="Weavo Liquid Loom logo" width="28" height="28"> Weavo Liquid Loom: Universal API

Convert CSV, JSON, and XML payloads between structured and text formats with Weavo Liquid Loom transformation recipes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weavoLiquidLoom/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weavo.net
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/weavoliquidloom/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [CSV to JSON](actions/csv-to-json.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavoLiquidLoom/latest/actions/csv-to-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputString": "Paste CSV input"
}'
```

## Actions (9)

### Csv To Json Result

| Action | Method | Description |
| --- | --- | --- |
| [CSV to JSON](actions/csv-to-json.md) | POST | Creates JSON output from CSV in Weavo Liquid Loom. |

### Csv To Text Result

| Action | Method | Description |
| --- | --- | --- |
| [CSV to Text](actions/csv-to-text.md) | POST | Creates text output from CSV in Weavo Liquid Loom. |

### Csv To Xml Result

| Action | Method | Description |
| --- | --- | --- |
| [CSV to XML](actions/csv-to-xml.md) | POST | Creates XML output from CSV in Weavo Liquid Loom. |

### Json To Json Result

| Action | Method | Description |
| --- | --- | --- |
| [JSON to JSON](actions/json-to-json.md) | POST | Creates JSON output from JSON in Weavo Liquid Loom. |

### Json To Text Result

| Action | Method | Description |
| --- | --- | --- |
| [JSON to Text](actions/json-to-text.md) | POST | Creates text output from JSON in Weavo Liquid Loom. |

### Json To Xml Result

| Action | Method | Description |
| --- | --- | --- |
| [JSON to XML](actions/json-to-xml.md) | POST | Creates XML output from JSON in Weavo Liquid Loom. |

### Xml To Json Result

| Action | Method | Description |
| --- | --- | --- |
| [XML to JSON](actions/xml-to-json.md) | POST | Creates JSON output from XML in Weavo Liquid Loom. |

### Xml To Text Result

| Action | Method | Description |
| --- | --- | --- |
| [XML to Text](actions/xml-to-text.md) | POST | Creates text output from XML in Weavo Liquid Loom. |

### Xml To Xml Result

| Action | Method | Description |
| --- | --- | --- |
| [XML to XML](actions/xml-to-xml.md) | POST | Creates XML output from XML in Weavo Liquid Loom. |

