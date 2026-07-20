# Plausible Analytics: Upsert Goal

Finds or creates a goal in a Plausible Analytics site.

```
PUT https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-goal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-goal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "goalType": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `goalType` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `PUT /api/v1/sites/goals` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-goal.md) for the provider-specific parameters and requirements.

