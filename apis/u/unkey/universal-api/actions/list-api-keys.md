# Unkey: List API keys

Retrieves API keys from Unkey for an API namespace.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-api-keys?connectionId=$CONNECTION_ID&limit=25&offset=0&apiId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "apiId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-api-keys?${params}`, {
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
| `apiId` | string | yes |  |

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
| `data[].createdAt` | number |  |
| `data[].credits` | object |  |
| `data[].credits.refill` | object |  |
| `data[].credits.refill.amount` | number |  |
| `data[].credits.refill.interval` | string |  |
| `data[].credits.refill.refillDay` | number |  |
| `data[].credits.remaining` | number |  |
| `data[].enabled` | boolean |  |
| `data[].expires` | number |  |
| `data[].identity` | object |  |
| `data[].identity.externalId` | string |  |
| `data[].identity.id` | string |  |
| `data[].identity.meta` | object |  |
| `data[].identity.ratelimits[]` | array<object> |  |
| `data[].identity.ratelimits[].autoApply` | boolean |  |
| `data[].identity.ratelimits[].duration` | number |  |
| `data[].identity.ratelimits[].id` | string |  |
| `data[].identity.ratelimits[].limit` | number |  |
| `data[].identity.ratelimits[].name` | string |  |
| `data[].keyId` | string |  |
| `data[].lastUsedAt` | number |  |
| `data[].meta` | object |  |
| `data[].name` | string |  |
| `data[].permissions[]` | array<string> |  |
| `data[].plaintext` | string |  |
| `data[].ratelimits[]` | array<object> |  |
| `data[].ratelimits[].autoApply` | boolean |  |
| `data[].ratelimits[].duration` | number |  |
| `data[].ratelimits[].id` | string |  |
| `data[].ratelimits[].limit` | number |  |
| `data[].ratelimits[].name` | string |  |
| `data[].roles[]` | array<string> |  |
| `data[].start` | string |  |
| `data[].updatedAt` | number |  |
| `meta` | object |  |
| `meta.requestId` | string |  |
| `pagination` | object |  |
| `pagination.cursor` | string |  |
| `pagination.hasMore` | boolean |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/apis.listKeys` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

