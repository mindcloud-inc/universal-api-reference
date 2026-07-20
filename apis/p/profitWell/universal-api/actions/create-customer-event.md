# ProfitWell: Create Customer Event

Creates a customer event in ProfitWell.

```
POST https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-customer-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-customer-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "cus_1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-customer-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "cus_1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The customer ID. Example: `cus_1234`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `POST https://api.profitwell-events.com/dotjs/v1/customer/event` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-event.md) for the provider-specific parameters and requirements.

