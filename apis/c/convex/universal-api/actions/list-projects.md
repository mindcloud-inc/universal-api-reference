# Convex: List Projects

Retrieves projects from a Convex team.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-projects?connectionId=$CONNECTION_ID&teamId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/list-projects?${params}`, {
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
| `teamId` | number | yes | The Convex team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": 1,
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "teamId": 1,
      "teamSlug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | number |  |
| `id` | number |  |
| `name` | string |  |
| `slug` | string |  |
| `teamId` | number |  |
| `teamSlug` | string |  |

## Native endpoint

Through the native Convex API, this operation is `GET /teams/:team_id/list_projects` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

