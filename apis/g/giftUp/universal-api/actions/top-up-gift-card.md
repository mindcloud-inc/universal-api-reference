# Gift Up: Top Up Gift Card



```
PUT https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/top-up-gift-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/top-up-gift-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "UQEZL"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/top-up-gift-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "UQEZL"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Example: `UQEZL`. |
| `amount` | number | no |  |
| `units` | number | no |  |
| `reason` | string | no |  |
| `locationId` | string | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "remainingCredit": 1,
      "remainingUnits": 1,
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `remainingCredit` | number |  |
| `remainingUnits` | number |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Gift Up API, this operation is `POST /gift-cards/:code/top-up` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/top-up-gift-card.md) for the provider-specific parameters and requirements.

