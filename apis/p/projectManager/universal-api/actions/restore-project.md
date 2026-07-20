# ProjectManager: Restore Project

Restores a deleted project in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/restore-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/restore-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11111111-1111-1111-1111-111111111111"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/restore-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11111111-1111-1111-1111-111111111111"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The unique identifier of the Project to delete Example: `11111111-1111-1111-1111-111111111111`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "additionalErrors": [
          "string"
        ],
        "message": "string",
        "technicalError": "string"
      },
      "hasError": true,
      "statusCode": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.additionalErrors` | array<string> |  |
| `error.message` | string |  |
| `error.technicalError` | string |  |
| `hasError` | boolean |  |
| `statusCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ProjectManager API, this operation is `PUT /api/data/projects/:projectId/restore` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-project.md) for the provider-specific parameters and requirements.

