# Codemagic: List Team App Previews

Retrieves app previews for a specific Codemagic team.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-app-previews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-app-previews?connectionId=$CONNECTION_ID&limit=25&offset=0&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-app-previews?${params}`, {
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
      "app": {},
      "artifact": {},
      "build": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "streaming_public_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `artifact` | object |  |
| `build` | object |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `expires_at` | date |  |
| `id` | string |  |
| `streaming_public_key` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/teams/:team_id/previews` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-app-previews.md) for the provider-specific parameters and requirements.

