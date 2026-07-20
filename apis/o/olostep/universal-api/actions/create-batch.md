# Olostep: Create Batch

Creates a new batch in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes | Array of batch items to process. Each item should include at least a URL and can optionally include a custom_id. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchCountry": "string",
      "batchParser": "string",
      "completedUrls": 1,
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "numberRetried": 1,
      "object": "string",
      "parser": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalUrls": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchCountry` | string |  |
| `batchParser` | string |  |
| `completedUrls` | number |  |
| `country` | string |  |
| `created` | date |  |
| `id` | string |  |
| `numberRetried` | number |  |
| `object` | string |  |
| `parser` | string |  |
| `startDate` | date |  |
| `status` | string |  |
| `totalUrls` | number |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/batches` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

