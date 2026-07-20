# LaunchDarkly: Search Contexts

Finds contexts in LaunchDarkly by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/search-contexts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/search-contexts?connectionId=$CONNECTION_ID&environmentKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/search-contexts?${params}`, {
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
      "_environmentId": "string",
      "_links": {},
      "continuationToken": "string",
      "items": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_environmentId` | string | The environment ID where the contexts were evaluated. |
| `_links` | object | Pagination and related resource links for the context search response. |
| `continuationToken` | string | Pagination token for fetching the next page of contexts. |
| `items` | array<object> | The collection of context records returned by the search. |
| `totalCount` | number | The number of matching contexts returned by the search. |

## Native endpoint

Through the native LaunchDarkly API, this operation is `POST /projects/:projectKey/environments/:environmentKey/contexts/search` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contexts.md) for the provider-specific parameters and requirements.

