# LaunchDarkly: List Segments

Retrieves segments from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-segments?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "environmentKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/list-segments?${params}`, {
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
| `environmentKey` | string | yes | The LaunchDarkly environment key. |
| `projectKey` | string | yes | The LaunchDarkly project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": 1,
      "deleted": true,
      "description": "string",
      "excluded": [
        "string"
      ],
      "excludedContexts": [
        {}
      ],
      "generation": 1,
      "included": [
        "string"
      ],
      "includedContexts": [
        {}
      ],
      "key": "string",
      "lastModifiedDate": 1,
      "links": {},
      "name": "Ava Chen",
      "rules": [
        {}
      ],
      "tags": [
        "string"
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `excluded` | array<string> |  |
| `excludedContexts` | array<object> |  |
| `generation` | number |  |
| `included` | array<string> |  |
| `includedContexts` | array<object> |  |
| `key` | string |  |
| `lastModifiedDate` | number |  |
| `links` | object |  |
| `name` | string |  |
| `rules` | array<object> |  |
| `tags` | array<string> |  |
| `version` | number |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /segments/:projectKey/:environmentKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

