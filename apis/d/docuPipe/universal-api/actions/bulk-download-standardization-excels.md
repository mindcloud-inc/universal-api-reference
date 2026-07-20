# DocuPipe: Bulk Download Standardization Excels

Creates bulk Excel download URLs for DocuPipe standardizations.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/bulk-download-standardization-excels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/bulk-download-standardization-excels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "standardizationIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/bulk-download-standardization-excels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "standardizationIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `standardizationIds[]` | array<string> | yes | List of standardization IDs to download as Excel files. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /standardization/download/bulk-excel` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-download-standardization-excels.md) for the provider-specific parameters and requirements.

