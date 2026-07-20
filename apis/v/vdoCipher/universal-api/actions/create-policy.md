# VdoCipher: Create Policy

Creates a new policy in VdoCipher.

```
POST https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/create-policy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainWhitelistMode` | string | no |  |
| `domainWhitelistOverride` | string | no |  |
| `domainWhitelistValues` | string | no |  |
| `geoEffect` | string | no |  |
| `geoList` | string | no |  |
| `name` | string | no |  |
| `rentalDuration` | string | no |  |
| `ttl` | string | no |  |
| `watermarkTemplate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domainWhitelistMode": "string",
      "domainWhitelistOverride": true,
      "domainWhitelistValues": [
        "string"
      ],
      "geoEffect": "string",
      "geoList": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "rentalDuration": 1,
      "ttl": 1,
      "updatedAt": "string",
      "watermarkTemplate": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `domainWhitelistMode` | string |  |
| `domainWhitelistOverride` | boolean |  |
| `domainWhitelistValues` | array<string> |  |
| `geoEffect` | string |  |
| `geoList` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `rentalDuration` | number |  |
| `ttl` | number |  |
| `updatedAt` | string |  |
| `watermarkTemplate` | array<string> |  |

## Native endpoint

Through the native VdoCipher API, this operation is `POST /policy` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-policy.md) for the provider-specific parameters and requirements.

