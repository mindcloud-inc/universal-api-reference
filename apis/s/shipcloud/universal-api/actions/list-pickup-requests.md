# Shipcloud: List Pickup Requests

Retrieves pickup requests from Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-pickup-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-pickup-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/list-pickup-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Shipcloud API, this operation is `GET /pickup_requests` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pickup-requests.md) for the provider-specific parameters and requirements.

