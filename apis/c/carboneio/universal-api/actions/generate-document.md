# Carbone.io: Generate Document

Creates a document from a stored Carbone.io template.

```
POST https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/generate-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Carbone.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/generate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "templateIdOrVersionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/carboneio/latest/actions/generate-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "templateIdOrVersionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `complement` | object | no | Additional JSON data exposed in the template as complement fields. |
| `convertTo` | string | no | Target format name such as pdf, docx, xlsx, html, csv, png, or webp. |
| `data` | object | yes | JSON dataset merged into the stored template. |
| `enum` | object | no | Enumeration map available to Carbone enum conversion helpers. |
| `lang` | string | no | Language code used for locale-aware formatting. |
| `reportName` | string | no | Output file name template for the generated report. |
| `templateIdOrVersionId` | string | yes | Template ID (64-bit) or Version ID (SHA-256) to render. |
| `timezone` | string | no | IANA timezone used when rendering date and time formatters. |
| `translations` | object | no | Localization dictionary used by translation tags in the template. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchOutput` | string | no | Output format for batch processing, such as zip or pdf. |
| `batchReportName` | string | no | File name template for each item produced by batch rendering. |
| `batchSplitBy` | string | no | JSON path used to split an array into multiple generated reports. |
| `converter` | string | no | Optional conversion engine override when Carbone exposes multiple converters. |
| `currencyRates` | object | no | Custom currency rates object used for conversion. |
| `currencySource` | string | no | Source currency code used when Carbone performs currency conversion. |
| `currencyTarget` | string | no | Target currency code used when Carbone performs currency conversion. |
| `hardRefresh` | boolean | no | Recompute pagination and table of contents after rendering. |
| `template` | string | no | Optional base64-encoded template contents to override the stored template at render time. |
| `variableStr` | string | no | Additional variable string passed to the render engine. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "renderId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `renderId` | string | Render ID used to retrieve the generated document later. |

## Native endpoint

Through the native Carbone.io API, this operation is `POST /render/[:templateId-or-versionId]` (base URL `https://api.carbone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-document.md) for the provider-specific parameters and requirements.

