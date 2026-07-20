# Autype: Create Bulk Render Job From JSON

Creates a bulk render job from JSON in Autype.

```
POST https://connect.mindcloud.co/v1/universal/autype/latest/actions/create-bulk-render-job-from-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autype/latest/actions/create-bulk-render-job-from-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "format": "string",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autype/latest/actions/create-bulk-render-job-from-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "format": "string",
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `format` | string | yes |  |
| `items[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkJobId": "string",
      "completedItems": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "failedItems": 1,
      "format": "string",
      "status": "string",
      "totalItems": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkJobId` | string |  |
| `completedItems` | number |  |
| `createdAt` | date |  |
| `failedItems` | number |  |
| `format` | string |  |
| `status` | string |  |
| `totalItems` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Autype API, this operation is `POST /bulk-render` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-render-job-from-json.md) for the provider-specific parameters and requirements.

