# Ghost: Update Tier

Updates an existing tier in Ghost.

```
PUT https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-tier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-tier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69b2eb888186310001a39583"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-tier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69b2eb888186310001a39583"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ghost tier ID from the URL path. Example: `69b2eb888186310001a39583`. |
| `tiers[0].name` | string | no | Updated tier name. Example: `Ghost Stage 3 Free Tier Updated`. |
| `tiers[0].description` | string | no | Updated public description for the tier. Example: `Updated temporary stage 3 tier`. |
| `tiers[0].active` | boolean | no | Whether the tier should remain active. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "id": "string",
      "monthlyPrice": 1,
      "name": "Ava Chen",
      "slug": "string",
      "trialDays": 1,
      "type": "string",
      "updatedAt": {},
      "visibility": "string",
      "welcomePageUrl": {},
      "yearlyPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | string |  |
| `monthlyPrice` | number |  |
| `name` | string |  |
| `slug` | string |  |
| `trialDays` | number |  |
| `type` | string |  |
| `updatedAt` | object |  |
| `visibility` | string |  |
| `welcomePageUrl` | object |  |
| `yearlyPrice` | number |  |

## Native endpoint

Through the native Ghost API, this operation is `PUT /tiers/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tier.md) for the provider-specific parameters and requirements.

