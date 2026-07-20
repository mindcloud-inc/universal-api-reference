# Codemagic: List Team Builds

Retrieves builds for a specific Codemagic team.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-builds?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-team-builds?${params}`, {
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
| `appId` | string | no | Optional application ID filter for team builds. |
| `workflowId` | string | no | Optional workflow ID filter for team builds. |
| `status` | string | no | Optional build status filter. |
| `branch` | string | no | Optional branch filter. |
| `tag` | string | no | Optional tag filter. |
| `label` | string | no | Optional build label filter. |
| `cursor` | string | no | Optional next-page cursor for team builds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_id": "string",
      "app_store_connect_status": "string",
      "artifacts": [
        {}
      ],
      "branch": "string",
      "commit": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "finished_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "index": 1,
      "labels": [
        "string"
      ],
      "release_notes": [
        {}
      ],
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tag": "string",
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_id` | string |  |
| `app_store_connect_status` | string |  |
| `artifacts` | array<object> |  |
| `branch` | string |  |
| `commit` | object |  |
| `created_at` | date |  |
| `finished_at` | date |  |
| `id` | string |  |
| `index` | number |  |
| `labels` | array<string> |  |
| `release_notes` | array<object> |  |
| `started_at` | date |  |
| `status` | string |  |
| `tag` | string |  |
| `workflow` | object |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/teams/:team_id/builds` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-builds.md) for the provider-specific parameters and requirements.

