# Unkey: List Identities

Retrieves all workspace identities from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-identities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-identities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-identities?${params}`, {
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
| `data[].externalId` | string |  |
| `data[].id` | string |  |
| `data[].meta` | object |  |
| `data[].ratelimits[]` | array<object> |  |
| `data[].ratelimits[].autoApply` | boolean |  |
| `data[].ratelimits[].duration` | number |  |
| `data[].ratelimits[].id` | string |  |
| `data[].ratelimits[].limit` | number |  |
| `data[].ratelimits[].name` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |
| `pagination` | object |  |
| `pagination.cursor` | string |  |
| `pagination.hasMore` | boolean |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/identities.listIdentities` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-identities.md) for the provider-specific parameters and requirements.

