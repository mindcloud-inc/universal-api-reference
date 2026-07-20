# Toggl Track: Create Client

Creates a new client in Toggl Track.

```
POST https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes |  |
| `name` | string | yes |  |
| `notes` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "at": "2026-05-07T12:00:00.000Z",
      "creatorId": 1,
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "totalCount": 1,
      "wid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the client is archived |
| `at` | date | Last updated timestamp |
| `creatorId` | number | Creator user ID |
| `id` | number | Client ID |
| `name` | string | Client name |
| `notes` | string | Client notes |
| `totalCount` | number | Client task count |
| `wid` | number | Workspace ID |

## Native endpoint

Through the native Toggl Track API, this operation is `POST /api/v9/workspaces/:workspace_id/clients` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

