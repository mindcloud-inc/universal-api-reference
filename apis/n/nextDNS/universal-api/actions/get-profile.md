# NextDNS: Get Profile

Retrieves a configuration profile from NextDNS.

```
GET https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile?${params}`, {
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
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowlist": [
        {}
      ],
      "denylist": [
        {}
      ],
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "parentalControl": {},
      "privacy": {},
      "rewrites": [
        {}
      ],
      "security": {},
      "settings": {},
      "setup": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowlist` | array<object> |  |
| `denylist` | array<object> |  |
| `fingerprint` | string |  |
| `id` | string |  |
| `name` | string |  |
| `parentalControl` | object |  |
| `privacy` | object |  |
| `rewrites` | array<object> |  |
| `security` | object |  |
| `settings` | object |  |
| `setup` | object |  |

## Native endpoint

Through the native NextDNS API, this operation is `GET /profiles/:profile` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

