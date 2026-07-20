# Svix: List Applications

Retrieves applications from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications?${params}`, {
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
| `excludeAppsWithNoEndpoints` | boolean | no | Exclude applications that have no endpoints. |
| `excludeAppsWithDisabledEndpoints` | boolean | no | Exclude applications that only have disabled endpoints. |
| `excludeAppsWithSvixPlayEndpoints` | boolean | no | Exclude applications that only have Svix Play endpoints. |
| `limit` | number | no | Maximum number of returned items. |
| `iterator` | string | no | Iterator returned from a prior invocation. |
| `order` | string | no | Sorting order for the returned applications. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "done": true,
      "iterator": "string",
      "prevIterator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `done` | boolean |  |
| `iterator` | string |  |
| `prevIterator` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/app` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

