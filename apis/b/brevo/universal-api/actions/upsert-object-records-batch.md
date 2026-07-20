# Brevo: Upsert Object Records Batch



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/upsert-object-records-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/upsert-object-records-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/upsert-object-records-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object_type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "processedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `processedCount` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/objects/:object_type/batch/upsert` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-object-records-batch.md) for the provider-specific parameters and requirements.

