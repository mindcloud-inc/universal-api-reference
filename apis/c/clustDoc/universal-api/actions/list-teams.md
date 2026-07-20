# ClustDoc: List Teams



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-teams?${params}`, {
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
      "cname_domain": "Ava Chen",
      "cname_status": 1,
      "id": 1,
      "name": "Ava Chen",
      "photo_url": "https://example.com",
      "user_current_team": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cname_domain` | string | The custom domain. |
| `cname_status` | number | The custom domain status. |
| `id` | number | The Clustdoc team ID. |
| `name` | string | The team name. |
| `photo_url` | string | The team avatar URL. |
| `user_current_team` | boolean | Whether this is the authenticated user's current team. |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /teams` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

