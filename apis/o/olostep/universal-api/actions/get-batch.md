# Olostep: Get Batch

Retrieves details for a batch in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-batch?connectionId=$CONNECTION_ID&batchId=batch_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "batch_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-batch?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchId` | string | yes | The ID of the batch to retrieve. Example: `batch_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
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
| `batchId` | string |  |
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

Through the native Olostep API, this operation is `GET /v1/batches/[:batch_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch.md) for the provider-specific parameters and requirements.

