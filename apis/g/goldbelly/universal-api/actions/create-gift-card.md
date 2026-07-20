# Goldbelly: Create Gift Card



```
POST https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/create-gift-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/create-gift-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/create-gift-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Gift card amount to create. |
| `recipientEmail` | string | no | Email address for the gift card recipient. |
| `message` | string | no | Optional message to include with the gift card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "balance": 1,
      "code": "string"
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

## Native endpoint

Through the native Goldbelly API, this operation is `POST gift_cards` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-gift-card.md) for the provider-specific parameters and requirements.

