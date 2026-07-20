# EasyPost: Get Pickup

Retrieves details for a pickup from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-pickup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-pickup?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-pickup?${params}`, {
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
| `id` | string | yes | EasyPost Pickup ID, beginning with pickup_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmation": "string",
      "id": "string",
      "maxDatetime": "2026-05-07T12:00:00.000Z",
      "minDatetime": "2026-05-07T12:00:00.000Z",
      "mode": "string",
      "object": "string",
      "pickupRates": [
        {}
      ],
      "reference": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmation` | string |  |
| `id` | string |  |
| `maxDatetime` | date |  |
| `minDatetime` | date |  |
| `mode` | string |  |
| `object` | string |  |
| `pickupRates` | array<object> |  |
| `reference` | string |  |
| `status` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /pickups/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pickup.md) for the provider-specific parameters and requirements.

