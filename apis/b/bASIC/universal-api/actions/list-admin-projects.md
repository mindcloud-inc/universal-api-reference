# BASIC: Get all admin projects of developer

Retrieves admin projects for the current developer in BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects?${params}`, {
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
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "profile": {
            "icon_url": "https://example.com",
            "styles": {
              "background_url": "https://example.com"
            }
          },
          "slug": "string",
          "team_id": "string",
          "team_name": "Ava Chen",
          "team_slug": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].profile.icon_url` | string |  |
| `data[].profile.styles.background_url` | string |  |
| `data[].slug` | string |  |
| `data[].team_id` | string |  |
| `data[].team_name` | string |  |
| `data[].team_slug` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /project/` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-admin-projects.md) for the provider-specific parameters and requirements.

