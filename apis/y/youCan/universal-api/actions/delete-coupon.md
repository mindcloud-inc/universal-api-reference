# YouCan: Delete Coupon

Deletes an existing coupon from YouCan.

```
DELETE https://connect.mindcloud.co/v1/universal/youCan/latest/actions/delete-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/delete-coupon?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/delete-coupon?${params}`, {
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
      "http_code": 1,
      "message": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `http_code` | number |  |
| `message` | string |  |
| `type` | string |  |

## Native endpoint

Through the native YouCan API, this operation is `DELETE /coupons/{id}` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-coupon.md) for the provider-specific parameters and requirements.

