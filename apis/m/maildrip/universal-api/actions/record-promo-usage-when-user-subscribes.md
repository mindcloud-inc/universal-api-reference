# Maildrip: Record promo usage when user subscribes



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/record-promo-usage-when-user-subscribes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/record-promo-usage-when-user-subscribes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "planId": "string",
  "pricePaid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/record-promo-usage-when-user-subscribes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "planId": "string",
    "pricePaid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planId` | string | yes | The plan ID the user subscribed to |
| `pricePaid` | number | yes | The actual price the user paid |
| `currency` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Promo usage recorded |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/promo/record-usage` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-promo-usage-when-user-subscribes.md) for the provider-specific parameters and requirements.

