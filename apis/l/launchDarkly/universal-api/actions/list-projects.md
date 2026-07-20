# LaunchDarkly: List Projects

Retrieves projects from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultClientSideAvailability": {},
      "id": "string",
      "includeInSnippetByDefault": true,
      "key": "string",
      "links": {},
      "name": "Ava Chen",
      "requireViewAssociationForNewFlags": true,
      "requireViewAssociationForNewSegments": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultClientSideAvailability` | object |  |
| `id` | string |  |
| `includeInSnippetByDefault` | boolean |  |
| `key` | string |  |
| `links` | object |  |
| `name` | string |  |
| `requireViewAssociationForNewFlags` | boolean |  |
| `requireViewAssociationForNewSegments` | boolean |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /projects` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

