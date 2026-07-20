# YouCan: Get Coupon

Retrieves details for a coupon from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-coupon?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-coupon?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "description": "string",
      "end_date": 1,
      "id": "string",
      "max_usage": 1,
      "start_date": 1,
      "status": "string",
      "type": 1,
      "type_text": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `description` | string |  |
| `end_date` | number |  |
| `id` | string |  |
| `max_usage` | number |  |
| `start_date` | number |  |
| `status` | string |  |
| `type` | number |  |
| `type_text` | string |  |
| `value` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /coupons/{id}` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon.md) for the provider-specific parameters and requirements.

