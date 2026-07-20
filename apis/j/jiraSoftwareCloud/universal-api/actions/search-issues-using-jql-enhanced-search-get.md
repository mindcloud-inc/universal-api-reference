# Jira Software Cloud: Search Issues Using JQL Enhanced Search (GET)

Finds issues in Jira Software Cloud using JQL.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-get?connectionId=$CONNECTION_ID&cloudId=string&jql=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "jql": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/search-issues-using-jql-enhanced-search-get?${params}`, {
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
| `jql` | string | yes | JQL query string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isLast": true,
      "issues": [
        {
          "id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isLast` | boolean |  |
| `issues[].id` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/search/jql` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-issues-using-jql-enhanced-search-get.md) for the provider-specific parameters and requirements.

