# Ghost: List Offers

Retrieves offers from Ghost.

```
GET https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-offers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/list-offers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cadence": "string",
      "code": "string",
      "createdAt": "string",
      "currency": {},
      "currencyRestriction": true,
      "displayDescription": "string",
      "displayTitle": "string",
      "duration": "string",
      "durationInMonths": {},
      "id": "string",
      "lastRedeemed": {},
      "name": "Ava Chen",
      "redemptionCount": 1,
      "redemptionType": "string",
      "status": "string",
      "tier": {
        "id": "string",
        "name": "Ava Chen"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cadence` | string |  |
| `code` | string |  |
| `createdAt` | string |  |
| `currency` | object |  |
| `currencyRestriction` | boolean |  |
| `displayDescription` | string |  |
| `displayTitle` | string |  |
| `duration` | string |  |
| `durationInMonths` | object |  |
| `id` | string |  |
| `lastRedeemed` | object |  |
| `name` | string |  |
| `redemptionCount` | number |  |
| `redemptionType` | string |  |
| `status` | string |  |
| `tier.id` | string |  |
| `tier.name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `GET /offers/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-offers.md) for the provider-specific parameters and requirements.

