# Plausible Analytics: List Goals

Retrieves goals from a Plausible Analytics site.

```
GET https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-goals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-goals?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Plausible Analytics API, this operation is `GET /api/v1/sites/goals` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-goals.md) for the provider-specific parameters and requirements.

