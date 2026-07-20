# NextDNS: Create Profile

Creates a new configuration profile in NextDNS.

```
POST https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/create-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/create-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Profile name. |
| `security` | object | no | Profile security settings object. |
| `privacy` | object | no | Profile privacy settings object. |
| `parentalControl` | object | no | Profile parental control settings object. |
| `denylist[]` | array<object> | no | Profile denylist array. |
| `allowlist[]` | array<object> | no | Profile allowlist array. |
| `settings` | object | no | Profile settings object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fingerprint` | string |  |
| `id` | string |  |
| `name` | string |  |
| `role` | string |  |

## Native endpoint

Through the native NextDNS API, this operation is `POST /profiles` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-profile.md) for the provider-specific parameters and requirements.

