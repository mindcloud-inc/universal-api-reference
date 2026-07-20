# Jira Software Cloud: Count Issues Using JQL

Retrieves an approximate JQL issue count from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/count-issues-using-jql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/count-issues-using-jql?connectionId=$CONNECTION_ID&cloudId=string&jql=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "jql": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/count-issues-using-jql?${params}`, {
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
| `jql` | string | yes | JQL query string to count. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `POST /ex/jira/:cloudId/rest/api/3/search/approximate-count` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-issues-using-jql.md) for the provider-specific parameters and requirements.

