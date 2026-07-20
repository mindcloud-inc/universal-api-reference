# Pushover: Cancel Emergency Receipt



```
PUT https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "receipt": "p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/cancel-emergency-receipt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "receipt": "p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receipt` | string | yes | Emergency notification receipt to cancel. Example: `p3v6Q9x2Lm4N8c1R5t7Y0z2Aa4Bb6C`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the receipt cancel request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /receipts/:receipt/cancel.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-emergency-receipt.md) for the provider-specific parameters and requirements.

