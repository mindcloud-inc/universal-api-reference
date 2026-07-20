# Unkey: Get Identity

Retrieves an identity record from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-identity?connectionId=$CONNECTION_ID&identity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identity": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-identity?${params}`, {
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
| `identity` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "externalId": "string",
        "id": "string",
        "meta": {},
        "ratelimits": [
          [
            {}
          ]
        ]
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
| `data.externalId` | string |  |
| `data.id` | string |  |
| `data.meta` | object |  |
| `data.ratelimits[]` | array<object> |  |
| `data.ratelimits[].autoApply` | boolean |  |
| `data.ratelimits[].duration` | number |  |
| `data.ratelimits[].id` | string |  |
| `data.ratelimits[].limit` | number |  |
| `data.ratelimits[].name` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/identities.getIdentity` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-identity.md) for the provider-specific parameters and requirements.

