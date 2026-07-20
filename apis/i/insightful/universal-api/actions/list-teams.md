# Insightful: List Teams

Retrieves teams from your Insightful account.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams?${params}`, {
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
      "default": true,
      "description": "string",
      "id": "string",
      "ignoreNeutral": true,
      "ignoreProductive": true,
      "ignoreUnproductive": true,
      "ignoreUnreviewed": true,
      "modelName": "Ava Chen",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `ignoreNeutral` | boolean |  |
| `ignoreProductive` | boolean |  |
| `ignoreUnproductive` | boolean |  |
| `ignoreUnreviewed` | boolean |  |
| `modelName` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Insightful API, this operation is `GET /team` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

