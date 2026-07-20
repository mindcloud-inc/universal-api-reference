# Gift Up: Undo Gift Card Redemption



```
PUT https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/undo-gift-card-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/undo-gift-card-redemption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "UQEZL",
  "transactionId": "1307602f-7bc5-44e4-baf1-08de8510b44b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/undo-gift-card-redemption', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "UQEZL",
    "transactionId": "1307602f-7bc5-44e4-baf1-08de8510b44b"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Example: `UQEZL`. |
| `transactionId` | string | yes | Example: `1307602f-7bc5-44e4-baf1-08de8510b44b`. |
| `reason` | string | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alreadyReversed": true,
      "amountReversed": 1,
      "remainingCredit": 1,
      "remainingUnits": 1,
      "transactionId": "string",
      "unitsReversed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alreadyReversed` | boolean |  |
| `amountReversed` | number |  |
| `remainingCredit` | number |  |
| `remainingUnits` | number |  |
| `transactionId` | string |  |
| `unitsReversed` | number |  |

## Native endpoint

Through the native Gift Up API, this operation is `POST /gift-cards/:code/undo-redemption` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/undo-gift-card-redemption.md) for the provider-specific parameters and requirements.

