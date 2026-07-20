# Jira Software Cloud: Get Projects Paginated

Retrieves projects from Jira Software Cloud.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-projects-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-projects-paginated?connectionId=$CONNECTION_ID&cloudId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/get-projects-paginated?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "isLast": true,
      "maxResults": 1,
      "startAt": 1,
      "total": 1,
      "values": [
        {
          "avatarUrls": {
            "48x48": "https://example.com"
          },
          "id": "string",
          "key": "string",
          "name": "Ava Chen",
          "projectTypeKey": "string"
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
| `maxResults` | number |  |
| `startAt` | number |  |
| `total` | number |  |
| `values[].avatarUrls.48x48` | string |  |
| `values[].id` | string |  |
| `values[].key` | string |  |
| `values[].name` | string |  |
| `values[].projectTypeKey` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /ex/jira/:cloudId/rest/api/3/project/search` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects-paginated.md) for the provider-specific parameters and requirements.

