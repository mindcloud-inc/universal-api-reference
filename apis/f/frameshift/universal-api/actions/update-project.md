# Frameshift: Update Project

Updates an existing project in Frameshift.

```
PUT https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | number | yes | Resource identifier for the project to access |
| `name` | string | no | The name of the project |
| `description` | string | no | The details surrounding the project |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "id": 1,
      "isCollection": true,
      "name": "Ava Chen",
      "nickname": {},
      "phiName": {},
      "primarySampleId": {},
      "uid": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isCollection` | boolean |  |
| `name` | string |  |
| `nickname` | object |  |
| `phiName` | object |  |
| `primarySampleId` | object |  |
| `uid` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `PUT /v1/projects/:project_id` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

