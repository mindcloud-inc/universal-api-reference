# Plausible Analytics: List Teams

Retrieves accessible teams from Plausible Analytics.

```
GET https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/list-teams?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `GET /api/v1/sites/teams` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

