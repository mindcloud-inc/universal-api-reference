# Ghost: Create Tier

Creates a new tier in Ghost.

```
POST https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-tier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-tier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tiers[0].name": "Ghost Stage 3 Free Tier"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-tier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tiers[0].name": "Ghost Stage 3 Free Tier"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tiers[0].name` | string | yes | Name of the tier. Example: `Ghost Stage 3 Free Tier`. |
| `tiers[0].description` | string | no | Public description for the tier. Example: `Temporary stage 3 tier`. |
| `tiers[0].welcomePageUrl` | string | no | Welcome page URL for the tier. Example: `https://mindcloud-1.ghost.io/welcome/ghost-stage-3-tier`. |
| `tiers[0].visibility` | string | no | Tier visibility, such as public or none. Example: `public`. |
| `tiers[0].monthlyPrice` | number | no | Monthly price in the smallest currency unit. Example: `500`. |
| `tiers[0].yearlyPrice` | number | no | Yearly price in the smallest currency unit. Example: `5000`. |
| `tiers[0].currency` | string | no | Three-letter ISO currency code for paid tiers. Example: `USD`. |
| `tiers[0].benefits[]` | array<string> | no | List of public benefits for the tier. Example: `Benefit one,Benefit two`. |
| `tiers[0].active` | boolean | no | Whether the tier should be active immediately. Example: `false`. |

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

Through the native Ghost API, this operation is `POST /tiers/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tier.md) for the provider-specific parameters and requirements.

