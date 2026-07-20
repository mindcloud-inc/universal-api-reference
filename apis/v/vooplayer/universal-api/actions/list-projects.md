# Vooplayer: List Projects

Retrieves projects from your Vooplayer account.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects?${params}`, {
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
      "archived": 1,
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "numberOfGB": 1,
      "numberOfSeconds": 1,
      "numberOfVideos": 1,
      "settings": 1,
      "theme": 1,
      "updated": "string",
      "userID": 1,
      "v3ID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | number | Archive flag. |
| `created` | string | Project creation timestamp. |
| `id` | number | Project ID. |
| `name` | string | Project name. |
| `numberOfGB` | number | Total storage used in gigabytes. |
| `numberOfSeconds` | number | Total seconds across project videos. |
| `numberOfVideos` | number | Number of videos in the project. |
| `settings` | number | Settings ID. |
| `theme` | number | Theme ID. |
| `updated` | string | Project update timestamp. |
| `userID` | number | Owner user ID. |
| `v3ID` | number | Provider v3 ID. |

## Native endpoint

Through the native Vooplayer API, this operation is `GET /groups` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

