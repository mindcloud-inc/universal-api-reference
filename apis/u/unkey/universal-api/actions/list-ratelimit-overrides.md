# Unkey: List ratelimit overrides

Retrieves rate limit overrides from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-ratelimit-overrides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-ratelimit-overrides?connectionId=$CONNECTION_ID&limit=25&offset=0&namespace=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "namespace": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-ratelimit-overrides?${params}`, {
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
| `namespace` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "meta": {
        "requestId": "string"
      },
      "pagination": {
        "cursor": "string",
        "hasMore": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].duration` | number |  |
| `data[].identifier` | string |  |
| `data[].limit` | number |  |
| `data[].overrideId` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |
| `pagination` | object |  |
| `pagination.cursor` | string |  |
| `pagination.hasMore` | boolean |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/ratelimit.listOverrides` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ratelimit-overrides.md) for the provider-specific parameters and requirements.

