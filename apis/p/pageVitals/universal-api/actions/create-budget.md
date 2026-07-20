# PageVitals: Create Budget



```
POST https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/create-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/create-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "metric": "string",
  "operator": "string",
  "value": "string",
  "device": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/create-budget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "metric": "string",
    "operator": "string",
    "value": "string",
    "device": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes |  |
| `metric` | string | yes |  |
| `operator` | string | yes |  |
| `value` | string | yes |  |
| `device` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device": "string",
      "id": "string",
      "metric": "string",
      "operator": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | string |  |
| `id` | string |  |
| `metric` | string |  |
| `operator` | string |  |
| `value` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `POST /:websiteId/budgets` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-budget.md) for the provider-specific parameters and requirements.

