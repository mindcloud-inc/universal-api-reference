# Codemagic: List OTA Projects

Retrieves over-the-air update projects for a Codemagic team.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-ota-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-ota-projects?connectionId=$CONNECTION_ID&limit=25&offset=0&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-ota-projects?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "deployment_channels": [
        {}
      ],
      "id": "string",
      "last_update": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployment_channels` | array<object> |  |
| `id` | string |  |
| `last_update` | date |  |
| `name` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/over-the-air-updates/:team_id/projects` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ota-projects.md) for the provider-specific parameters and requirements.

