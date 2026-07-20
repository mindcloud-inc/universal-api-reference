# Openlayer: Update Project User Tag

Updates an existing project user tag in Openlayer.

```
PUT https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/update-project-user-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/update-project-user-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "tagId": "23ad6273-c293-48fc-b44a-f7419da3f866"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/update-project-user-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
    "tagId": "23ad6273-c293-48fc-b44a-f7419da3f866"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no | Updated tag color. Default: `green`. |
| `name` | string | no | Updated tag name. Default: `MindCloud Tag Updated`. |
| `projectId` | string | yes | The Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `tagId` | string | yes | The user tag ID. Default: `23ad6273-c293-48fc-b44a-f7419da3f866`. |

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

Through the native Openlayer API, this operation is `PUT /projects/:projectId/user-tags/:tagId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-user-tag.md) for the provider-specific parameters and requirements.

