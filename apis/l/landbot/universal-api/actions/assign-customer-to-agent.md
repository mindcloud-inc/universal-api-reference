# Landbot: Assign Customer to Agent

Assigns a customer to an agent in Landbot.

```
PUT https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "agentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landbot/latest/actions/assign-customer-to-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "agentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Customer ID to assign. |
| `agentId` | number | yes | Agent ID to assign the customer to. |

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

Through the native Landbot API, this operation is `PUT /v1/customers/:customer_id/assign/:agent_id/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-customer-to-agent.md) for the provider-specific parameters and requirements.

