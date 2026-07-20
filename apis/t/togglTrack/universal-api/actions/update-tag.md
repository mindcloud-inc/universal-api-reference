# Toggl Track: Update Tag

Updates an existing tag in Toggl Track.

```
PUT https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "tagId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "tagId": 1,
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
| `tagId` | list<number> | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "at": "string",
      "creatorId": 1,
      "id": 1,
      "name": "Ava Chen",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `at` | string | Last updated timestamp |
| `creatorId` | number | Creator user ID |
| `id` | number | Tag ID |
| `name` | string | Tag name |
| `workspaceId` | number | Workspace ID |

## Native endpoint

Through the native Toggl Track API, this operation is `PUT /api/v9/workspaces/:workspace_id/tags/:tag_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

