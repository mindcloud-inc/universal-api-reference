# Scale: Set Batch Metadata



```
PUT https://connect.mindcloud.co/v1/universal/scale/latest/actions/set-batch-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scale/latest/actions/set-batch-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metadata": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scale/latest/actions/set-batch-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metadata": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | yes | Metadata object to store on the batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Scale API, this operation is `POST /v2/batch/metadata` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-batch-metadata.md) for the provider-specific parameters and requirements.

