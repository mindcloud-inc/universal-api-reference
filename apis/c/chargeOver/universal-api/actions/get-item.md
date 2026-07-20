# ChargeOver: Get Item

Retrieves detailed item records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-item?${params}`, {
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
| `itemId` | number | yes | The ChargeOver item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "enabled": true,
      "item_id": 1,
      "item_type": "string",
      "name": "Ava Chen",
      "service_dates_type": "string",
      "token": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `enabled` | boolean |  |
| `item_id` | number |  |
| `item_type` | string |  |
| `name` | string |  |
| `service_dates_type` | string |  |
| `token` | string |  |
| `units` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /item/:item_id` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

