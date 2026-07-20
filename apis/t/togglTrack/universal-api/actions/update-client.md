# Toggl Track: Update Client

Updates an existing client in Toggl Track.

```
PUT https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<number> | yes |  |
| `clientId` | list<number> | yes |  |
| `name` | string | no |  |
| `notes` | string | no |  |
| `externalReference` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "at": "string",
      "creatorId": 1,
      "id": 1,
      "name": "Ava Chen",
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
| `archived` | boolean |  |
| `at` | string |  |
| `creatorId` | number |  |
| `id` | number |  |
| `name` | string |  |
| `totalCount` | number |  |
| `wid` | number |  |

## Native endpoint

Through the native Toggl Track API, this operation is `PUT /api/v9/workspaces/:workspace_id/clients/:client_id` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

