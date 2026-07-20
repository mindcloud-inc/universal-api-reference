# EasyPost: Create Batch

Creates a new batch in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batch": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batch": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batch` | object | yes | Batch object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelUrl": "https://example.com",
      "mode": "string",
      "numShipments": 1,
      "object": "string",
      "scanForm": {},
      "shipments": [
        {}
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelUrl` | string |  |
| `mode` | string |  |
| `numShipments` | number |  |
| `object` | string |  |
| `scanForm` | object |  |
| `shipments` | array<object> |  |
| `state` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /batches` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

