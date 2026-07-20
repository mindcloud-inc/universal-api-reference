# Jira Software Cloud: Create Issue

Creates a new issue in Jira Software Cloud.

```
POST https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Jira cloud site ID returned by Accessible Resources. |
| `fields` | object | yes | Issue fields object for the new issue. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `key` | string |  |
| `self` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `POST /ex/jira/:cloudId/rest/api/3/issue` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

