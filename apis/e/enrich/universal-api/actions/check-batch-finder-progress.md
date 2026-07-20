# Enrich.so: Check Batch Finder Progress

Retrieves batch email finder progress from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-batch-finder-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-batch-finder-progress?connectionId=$CONNECTION_ID&batchId=665a1f4e2c3b7800129dce01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "665a1f4e2c3b7800129dce01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-batch-finder-progress?${params}`, {
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
| `batchId` | string | yes | Batch ID returned by the batch email finder submit action. Default: `665a1f4e2c3b7800129dce01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "processedItems": 1,
      "progress": 1,
      "status": "string",
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string | Email finder batch identifier. |
| `processedItems` | number | Leads processed so far. |
| `progress` | number | Completion percentage from 0 to 100. |
| `status` | string | Current batch status. |
| `totalItems` | number | Total leads in the batch. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /email-finder/batch/{batchId}` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-batch-finder-progress.md) for the provider-specific parameters and requirements.

