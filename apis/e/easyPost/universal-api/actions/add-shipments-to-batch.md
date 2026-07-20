# EasyPost: Add Shipments To Batch

Adds shipments to an existing batch in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/add-shipments-to-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/add-shipments-to-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "shipments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/add-shipments-to-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "shipments[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EasyPost Batch ID, beginning with batch_. |
| `shipments[]` | array<object> | yes | Shipments to add to the batch. |

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

Through the native EasyPost API, this operation is `POST /batches/:id/add_shipments` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-shipments-to-batch.md) for the provider-specific parameters and requirements.

