# ProjectManager: Delete Project

Deletes an existing project from ProjectManager.

```
DELETE https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-project?connectionId=$CONNECTION_ID&projectId=11111111-1111-1111-1111-111111111111" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "11111111-1111-1111-1111-111111111111"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/delete-project?${params}`, {
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
| `projectId` | string | yes | The unique identifier of the Project to delete Example: `11111111-1111-1111-1111-111111111111`. |
| `hardDelete` | boolean | no | Hard delete project true or false Example: `true`. |

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

Through the native ProjectManager API, this operation is `DELETE /api/data/projects/:projectId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

