# Jira Software Cloud: Get Project Statuses

Retrieves project statuses from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project-statuses?connectionId=$CONNECTION_ID&cloudId=string&projectIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "projectIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-project-statuses?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "statuses": [
        {
          "description": "string",
          "iconUrl": "https://example.com",
          "id": "string",
          "name": "Ava Chen",
          "scope": {
            "project": {
              "id": "string"
            }
          },
          "statusCategory": {
            "key": "string"
          }
        }
      ],
      "subtask": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `statuses[].description` | string |  |
| `statuses[].iconUrl` | string |  |
| `statuses[].id` | string |  |
| `statuses[].name` | string |  |
| `statuses[].scope.project.id` | string |  |
| `statuses[].statusCategory.key` | string |  |
| `subtask` | boolean |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/project/:projectIdOrKey/statuses` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-statuses.md) for the provider-specific parameters and requirements.

