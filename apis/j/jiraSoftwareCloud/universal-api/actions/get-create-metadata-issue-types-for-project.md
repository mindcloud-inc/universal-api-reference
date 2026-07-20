# Jira Software Cloud: Get Create Metadata Issue Types For Project

Retrieves project issue types for Jira Software Cloud issue creation.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-create-metadata-issue-types-for-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-create-metadata-issue-types-for-project?connectionId=$CONNECTION_ID&cloudId=string&projectIdOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "projectIdOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-create-metadata-issue-types-for-project?${params}`, {
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
      "issueTypes": [
        {
          "description": "string",
          "hierarchyLevel": 1,
          "iconUrl": "https://example.com",
          "id": "string",
          "name": "Ava Chen",
          "scope": {
            "project": {
              "id": "string"
            }
          },
          "subtask": true
        }
      ],
      "maxResults": 1,
      "startAt": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issueTypes[].description` | string |  |
| `issueTypes[].hierarchyLevel` | number |  |
| `issueTypes[].iconUrl` | string |  |
| `issueTypes[].id` | string |  |
| `issueTypes[].name` | string |  |
| `issueTypes[].scope.project.id` | string |  |
| `issueTypes[].subtask` | boolean |  |
| `maxResults` | number |  |
| `startAt` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/issue/createmeta/:projectIdOrKey/issuetypes` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-create-metadata-issue-types-for-project.md) for the provider-specific parameters and requirements.

