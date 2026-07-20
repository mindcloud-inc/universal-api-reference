# Frameshift: Get Project File URL

Retrieves a project file URL from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-project-file-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-project-file-url?connectionId=$CONNECTION_ID&projectId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/get-project-file-url?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `fileId` | string | yes | Resource identifier for the file to access |
| `createActivity` | boolean | no | If set to true will create a project activity |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/files/:file_id/url` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-file-url.md) for the provider-specific parameters and requirements.

