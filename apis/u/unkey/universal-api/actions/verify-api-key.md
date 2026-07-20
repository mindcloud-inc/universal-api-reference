# Unkey: Verify API key

Verifies an API key in Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/verify-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/verify-api-key?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/verify-api-key?${params}`, {
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
| `key` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "code": "string",
        "credits": 1,
        "enabled": true,
        "expires": 1,
        "identity": {
          "externalId": "string",
          "id": "string",
          "meta": {},
          "ratelimits": [
            [
              {}
            ]
          ]
        },
        "keyId": "string",
        "meta": {},
        "name": "Ava Chen",
        "permissions": [
          [
            "string"
          ]
        ],
        "ratelimits": [
          [
            {}
          ]
        ],
        "roles": [
          [
            "string"
          ]
        ],
        "valid": true
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.code` | string |  |
| `data.credits` | number |  |
| `data.enabled` | boolean |  |
| `data.expires` | number |  |
| `data.identity` | object |  |
| `data.identity.externalId` | string |  |
| `data.identity.id` | string |  |
| `data.identity.meta` | object |  |
| `data.identity.ratelimits[]` | array<object> |  |
| `data.identity.ratelimits[].autoApply` | boolean |  |
| `data.identity.ratelimits[].duration` | number |  |
| `data.identity.ratelimits[].id` | string |  |
| `data.identity.ratelimits[].limit` | number |  |
| `data.identity.ratelimits[].name` | string |  |
| `data.keyId` | string |  |
| `data.meta` | object |  |
| `data.name` | string |  |
| `data.permissions[]` | array<string> |  |
| `data.ratelimits[]` | array<object> |  |
| `data.ratelimits[].autoApply` | boolean |  |
| `data.ratelimits[].duration` | number |  |
| `data.ratelimits[].exceeded` | boolean |  |
| `data.ratelimits[].id` | string |  |
| `data.ratelimits[].limit` | number |  |
| `data.ratelimits[].name` | string |  |
| `data.ratelimits[].remaining` | number |  |
| `data.ratelimits[].reset` | number |  |
| `data.roles[]` | array<string> |  |
| `data.valid` | boolean |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/keys.verifyKey` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-api-key.md) for the provider-specific parameters and requirements.

