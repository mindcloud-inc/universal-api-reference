# Peach: Update Subscription Additional Sum

Updates a subscription payment in Peach with a new recurring sum.

```
PUT https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-subscription-additional-sum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-subscription-additional-sum" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentId": "string",
  "updatedSum": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/update-subscription-additional-sum', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentId": "string",
    "updatedSum": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentId` | string | yes | The payment ID to update. |
| `updatedSum` | number | yes | New recurring sum for the subscription. |

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
| `message` | string |  |

## Native endpoint

Through the native Peach API, this operation is `PUT /payment/:paymentId` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription-additional-sum.md) for the provider-specific parameters and requirements.

