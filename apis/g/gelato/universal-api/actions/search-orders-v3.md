# Gelato: Search Orders v3

Finds orders in Gelato v3 by filters.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/search-orders-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/search-orders-v3?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/search-orders-v3?${params}`, {
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
| `ids[]` | array<string> | no |  |
| `orderReferenceId` | string | no |  |
| `orderReferenceIds[]` | array<string> | no |  |
| `orderTypes[]` | array<string> | no |  |
| `channels[]` | array<string> | no |  |
| `countries[]` | array<string> | no |  |
| `financialStatuses[]` | array<string> | no |  |
| `fulfillmentStatuses[]` | array<string> | no |  |
| `search` | string | no |  |
| `startDate` | string | no |  |
| `endDate` | string | no |  |
| `storeIds[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `POST /v3/orders:search` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-orders-v3.md) for the provider-specific parameters and requirements.

