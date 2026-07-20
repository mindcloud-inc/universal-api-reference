# VdoCipher: Update Policy

Updates an existing policy in VdoCipher.

```
PUT https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/update-policy', {
  method: 'PUT',
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
| `id` | string | no |  |
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `PUT /policy/:id` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-policy.md) for the provider-specific parameters and requirements.

