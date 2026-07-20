# Unkey: Get API key

Retrieves an API key from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-key?connectionId=$CONNECTION_ID&keyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-key?${params}`, {
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
| `keyId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": 1,
        "credits": {
          "refill": {
            "amount": 1,
            "interval": "string",
            "refillDay": 1
          },
          "remaining": 1
        },
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
        "lastUsedAt": 1,
        "meta": {},
        "name": "Ava Chen",
        "permissions": [
          [
            "string"
          ]
        ],
        "plaintext": "string",
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
        "start": "string",
        "updatedAt": 1
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
| `data.createdAt` | number |  |
| `data.credits` | object |  |
| `data.credits.refill` | object |  |
| `data.credits.refill.amount` | number |  |
| `data.credits.refill.interval` | string |  |
| `data.credits.refill.refillDay` | number |  |
| `data.credits.remaining` | number |  |
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
| `data.lastUsedAt` | number |  |
| `data.meta` | object |  |
| `data.name` | string |  |
| `data.permissions[]` | array<string> |  |
| `data.plaintext` | string |  |
| `data.ratelimits[]` | array<object> |  |
| `data.ratelimits[].autoApply` | boolean |  |
| `data.ratelimits[].duration` | number |  |
| `data.ratelimits[].id` | string |  |
| `data.ratelimits[].limit` | number |  |
| `data.ratelimits[].name` | string |  |
| `data.roles[]` | array<string> |  |
| `data.start` | string |  |
| `data.updatedAt` | number |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/keys.getKey` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key.md) for the provider-specific parameters and requirements.

