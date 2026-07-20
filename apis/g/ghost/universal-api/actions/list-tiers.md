# Ghost: List Tiers

Retrieves tiers from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-tiers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-tiers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-tiers?${params}`, {
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
| `include` | string | no | Comma-separated related tier resources to include, such as monthly_price, yearly_price, or benefits. |
| `filter` | string | no | Ghost filter expression for narrowing tiers by type, visibility, or active status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "currency": "string",
      "description": {},
      "id": "string",
      "monthlyPrice": 1,
      "name": "Ava Chen",
      "slug": "string",
      "trialDays": 1,
      "type": "string",
      "updatedAt": "string",
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
| `description` | object |  |
| `id` | string |  |
| `monthlyPrice` | number |  |
| `name` | string |  |
| `slug` | string |  |
| `trialDays` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `visibility` | string |  |
| `welcomePageUrl` | object |  |
| `yearlyPrice` | number |  |

## Native endpoint

Through the native Ghost API, this operation is `GET /tiers/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tiers.md) for the provider-specific parameters and requirements.

