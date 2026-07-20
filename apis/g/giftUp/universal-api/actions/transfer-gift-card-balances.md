# Gift Up: Transfer Gift Card Balances



```
PUT https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/transfer-gift-card-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/transfer-gift-card-balances" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceGiftCards[]": [
    "string"
  ],
  "destinationGiftCard": "ABC789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/transfer-gift-card-balances', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceGiftCards[]": ["string"],
    "sourceGiftCards[]": ["string"],
    "sourceGiftCards[]": ["string"],
    "destinationGiftCard": "ABC789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceGiftCards[]` | array<string> | yes | Gift card codes to transfer balances from. |
| `sourceGiftCards[]` | array<string> | yes | Gift card codes to transfer balances from. |
| `sourceGiftCards[]` | array<string> | yes | Gift card codes to transfer balances from. |
| `destinationGiftCard` | string | yes | Example: `ABC789`. |
| `reason` | string | no |  |
| `locationId` | string | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transferredUnits": 1,
      "transferredValue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transferredUnits` | number |  |
| `transferredValue` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `POST /gift-cards/transfer-balances` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-gift-card-balances.md) for the provider-specific parameters and requirements.

