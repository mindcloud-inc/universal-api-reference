# Jira Software Cloud: Edit Issue

Updates an existing issue in Jira Software Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/edit-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/edit-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "issueIdOrKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/edit-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "issueIdOrKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |
| `fields` | object | no | Issue fields object to update. |
| `issueIdOrKey` | string | yes | Issue ID or key such as PROJ-123. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnIssue` | boolean | no | When true, Jira returns the updated issue in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expand": "string",
      "fields": {
        "summary": "string"
      },
      "id": "string",
      "key": "string",
      "self": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expand` | string |  |
| `fields.summary` | string |  |
| `id` | string |  |
| `key` | string |  |
| `self` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `PUT /ex/jira/:cloudId/rest/api/3/issue/:issueIdOrKey` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-issue.md) for the provider-specific parameters and requirements.

