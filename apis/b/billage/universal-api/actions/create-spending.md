# Billage: Create Spending

Creates a new spending in Billage.

```
POST https://connect.mindcloud.co/v1/universal/billage/latest/actions/create-spending
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billage/latest/actions/create-spending" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spending": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billage/latest/actions/create-spending', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spending": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spending` | object | yes | Spending payload |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billage API returns.

## Native endpoint

Through the native Billage API, this operation is `POST /v2/spendings` (base URL `https://app.getbillage.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-spending.md) for the provider-specific parameters and requirements.

