# LaunchDarkly: Get Context

Retrieves a context from LaunchDarkly by kind and key.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-context?connectionId=$CONNECTION_ID&environmentKey=string&key=string&kind=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentKey": "string",
  "key": "string",
  "kind": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-context?${params}`, {
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
| `key` | string | yes | The LaunchDarkly context key. |
| `kind` | string | yes | The LaunchDarkly context kind. |
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
| `_environmentId` | string | The environment ID where the context was evaluated. |
| `_links` | object | Pagination and related resource links for the context lookup response. |
| `continuationToken` | string | Pagination token for fetching the next page of contexts. |
| `items` | array<object> | The collection of context records returned by the lookup. |
| `totalCount` | number | The number of contexts returned for the lookup. |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /projects/:projectKey/environments/:environmentKey/contexts/:kind/:key` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-context.md) for the provider-specific parameters and requirements.

