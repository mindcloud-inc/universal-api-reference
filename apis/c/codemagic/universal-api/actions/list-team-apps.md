# Codemagic: List Team Apps

Retrieves apps for a specific Codemagic team.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-apps?connectionId=$CONNECTION_ID&limit=25&offset=0&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-apps?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Codemagic team identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Optional app ID filter documented by Codemagic for team apps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "icon_url": "https://example.com",
      "id": "string",
      "last_build_id": "string",
      "name": "Ava Chen",
      "project_type": "string",
      "repository": {},
      "settings_source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `icon_url` | string |  |
| `id` | string |  |
| `last_build_id` | string |  |
| `name` | string |  |
| `project_type` | string |  |
| `repository` | object |  |
| `settings_source` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/teams/:team_id/apps` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-apps.md) for the provider-specific parameters and requirements.

