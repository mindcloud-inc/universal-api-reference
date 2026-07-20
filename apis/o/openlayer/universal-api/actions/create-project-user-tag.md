# Openlayer: Create Project User Tag

Creates a new user tag for a project in Openlayer.

```
POST https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-user-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-user-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "color": "blue",
  "name": "MindCloud Runtime Tag",
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-project-user-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "color": "blue",
    "name": "MindCloud Runtime Tag",
    "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | yes | The tag color. Default: `blue`. |
| `name` | string | yes | The name of the user tag. Default: `MindCloud Runtime Tag`. |
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "creatorId": "string",
      "dateCreated": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `creatorId` | string |  |
| `dateCreated` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `POST /projects/:projectId/user-tags` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-user-tag.md) for the provider-specific parameters and requirements.

