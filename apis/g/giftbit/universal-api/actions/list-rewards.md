# Giftbit: List Rewards

Lists rewards in your Giftbit account.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-rewards?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-rewards?${params}`, {
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
| `uuid` | string | no |  |
| `campaignUuid` | string | no |  |
| `campaignId` | string | no |  |
| `recipientName` | string | no |  |
| `recipientEmail` | string | no |  |
| `deliveryStatus` | string | no |  |
| `status` | string | no |  |
| `priceInCentsGreaterThan` | number | no |  |
| `priceInCentsLessThan` | number | no |  |
| `createdDateGreaterThan` | date | no |  |
| `createdDateLessThan` | date | no |  |
| `deliveryDateGreaterThan` | date | no |  |
| `deliveryDateLessThan` | date | no |  |
| `redeemedDateGreaterThan` | date | no |  |
| `redeemedDateLessThan` | date | no |  |
| `redeliveryCountGreaterThan` | number | no |  |
| `redeliveryCountLessThan` | number | no |  |
| `sort` | string | no |  |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gifts": [
        {}
      ],
      "info": {},
      "limit": 1,
      "number_of_results": 1,
      "offset": 1,
      "status": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gifts` | array<object> |  |
| `info` | object |  |
| `limit` | number |  |
| `number_of_results` | number |  |
| `offset` | number |  |
| `status` | number |  |
| `total_count` | number |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /gifts` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-rewards.md) for the provider-specific parameters and requirements.

