# Calculoid: Rate Calculator



```
PUT https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/rate-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/rate-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calculatorId": "109359",
  "rating": "5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/rate-calculator', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calculatorId": "109359",
    "rating": "5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calculatorId` | string | yes | Calculoid calculator ID. Default: `0`. Example: `109359`. |
| `rating` | number | yes | Numeric calculator rating. Default: `5`. Example: `5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calculoid API returns.

## Native endpoint

Through the native Calculoid API, this operation is `POST /calculator/rate/:calculatorId` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rate-calculator.md) for the provider-specific parameters and requirements.

