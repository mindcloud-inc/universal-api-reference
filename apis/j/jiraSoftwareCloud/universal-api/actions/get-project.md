# Jira Software Cloud: Get Project

Retrieves a project from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project?connectionId=$CONNECTION_ID&cloudId=string&projectIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "projectIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project?${params}`, {
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
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |
| `projectIdOrKey` | string | yes | Project ID or key such as ENG. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrls": {
        "48x48": "https://example.com"
      },
      "description": "string",
      "id": "string",
      "isPrivate": true,
      "key": "string",
      "name": "Ava Chen",
      "projectTypeKey": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrls.48x48` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `projectTypeKey` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

