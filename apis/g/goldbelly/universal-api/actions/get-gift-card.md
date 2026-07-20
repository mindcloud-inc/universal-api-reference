# Goldbelly: Get Gift Card



```
GET https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-gift-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-gift-card?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/get-gift-card?${params}`, {
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
| `code` | string | yes | Gift card code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "balance": 1,
      "code": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `balance` | number |  |
| `code` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Goldbelly API, this operation is `GET gift_cards/:code` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gift-card.md) for the provider-specific parameters and requirements.

