# mittwald: List Project Filesystem Directories

Retrieves project filesystem directories from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-filesystem-directories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-filesystem-directories?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-project-filesystem-directories?${params}`, {
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
| `projectId` | string | yes | The unique identifier of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "absolutePath": "string",
      "isDirectory": true,
      "isFile": true,
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absolutePath` | string |  |
| `isDirectory` | boolean |  |
| `isFile` | boolean |  |
| `name` | string |  |
| `size` | number |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/projects/:projectId/filesystem-directories` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-filesystem-directories.md) for the provider-specific parameters and requirements.

