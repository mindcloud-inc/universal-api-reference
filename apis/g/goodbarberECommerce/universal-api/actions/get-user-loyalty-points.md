# Goodbarber eCommerce: Get User Loyalty Points



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-user-loyalty-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-user-loyalty-points?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-user-loyalty-points?${params}`, {
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
| `userId` | number | yes | Unique ID of the user. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "points_count": 1,
      "points_expiry_dt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `points_count` | number | <div class="field_description">Amount of loyalty points the user has accumulated.</div> |
| `points_expiry_dt` | string | <div class="field_description">Expiration date of the user loyalty points with format <code>%Y-%m-%dT%H:%M:%SZ</code></div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/marketing/:webzine_id/loyalty/user/:user_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-loyalty-points.md) for the provider-specific parameters and requirements.

