# Launch27: Check Gift Card Discount

Checks a gift card discount in Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/check-gift-card-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/check-gift-card-discount?connectionId=$CONNECTION_ID&email=ava%40example.com&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/check-gift-card-discount?${params}`, {
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
| `email` | string | yes | Sender email used to validate the gift card discount code. |
| `code` | string | yes | Gift card discount code to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "percent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `percent` | number |  |

## Native endpoint

Through the native Launch27 API, this operation is `POST giftcard/discount` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-gift-card-discount.md) for the provider-specific parameters and requirements.

