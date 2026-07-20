# BugHerd: Update Project

Updates an existing project in BugHerd.

```
PUT https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BugHerd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bugHerd/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The BugHerd project ID. |
| `project` | object | no | Project fields to update. |
| `project.is_public` | boolean | no | Enable or disable public feedback. |
| `project.permission` | string | no | Guest visibility permission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "devurl": "https://example.com",
      "guestsSeeGuests": true,
      "id": 1,
      "isActive": true,
      "isPublic": true,
      "name": "Ava Chen",
      "ownerName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `devurl` | string |  |
| `guestsSeeGuests` | boolean |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `ownerName` | string |  |

## Native endpoint

Through the native BugHerd API, this operation is `PUT projects/:project_id.json` (base URL `https://www.bugherd.com/api_v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

