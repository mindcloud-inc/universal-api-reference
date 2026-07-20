# KiteSuite: Update Project

Updates an existing project in KiteSuite.

```
PUT https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "projectName": "Ava Chen",
  "projectType": "string",
  "projectLead": "string",
  "avatar": "default.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "projectName": "Ava Chen",
    "projectType": "string",
    "projectLead": "string",
    "avatar": "default.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Project ID. |
| `projectName` | string | yes | Updated project name. |
| `projectType` | string | yes | Project type. |
| `projectLead` | string | yes | User ID of the project lead. |
| `avatar` | string | yes | Project avatar filename. Default: `default.png`. |
| `favorite` | boolean | no | Whether the project is favorited. |
| `description` | string | no | Updated project description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "description": "string",
      "favorite": true,
      "key": "string",
      "platform": "string",
      "projectName": "Ava Chen",
      "projectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `description` | string |  |
| `favorite` | boolean |  |
| `key` | string |  |
| `platform` | string |  |
| `projectName` | string |  |
| `projectType` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `PUT /api/v1/project/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

