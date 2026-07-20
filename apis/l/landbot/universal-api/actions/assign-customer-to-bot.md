# Landbot: Assign Customer to Bot

Assigns a customer to a bot in Landbot.

```
PUT https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "botId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-bot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "botId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Customer ID to assign. |
| `botId` | number | yes | Bot ID to assign the customer to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Landbot API, this operation is `PUT /v1/customers/:customer_id/assign_bot/:bot_id/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-customer-to-bot.md) for the provider-specific parameters and requirements.

