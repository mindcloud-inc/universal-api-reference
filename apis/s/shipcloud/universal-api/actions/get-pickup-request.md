# Shipcloud: Get Pickup Request

Retrieves a pickup request from Shipcloud by ID.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-pickup-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-pickup-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-pickup-request?${params}`, {
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
| `id` | string | yes | The Shipcloud pickup request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrier_pickup_number": "string",
      "id": "string",
      "pickup_address": {},
      "pickup_time": {},
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_pickup_number` | string |  |
| `id` | string |  |
| `pickup_address` | object |  |
| `pickup_time` | object |  |
| `shipments` | array<object> |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /pickup_requests/:id` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pickup-request.md) for the provider-specific parameters and requirements.

