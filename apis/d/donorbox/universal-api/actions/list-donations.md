# Donorbox: List Donations

Retrieves donations from Donorbox.

```
GET https://connect.mindcloud.co/v1/universal/donorbox/latest/actions/list-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Donorbox `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/donorbox/latest/actions/list-donations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/donorbox/latest/actions/list-donations?${params}`, {
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
| `id` | string | no |  |
| `email` | list<string> | no |  |
| `dateFrom` | string | no |  |
| `dateTo` | string | no |  |
| `campaignId` | list<string> | no |  |
| `campaignName` | string | no |  |
| `donorId` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `amountUsdMin` | string | no | Minimum USD amount filter. |
| `amountUsdMax` | string | no | Maximum USD amount filter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Donorbox API returns.

## Native endpoint

Through the native Donorbox API, this operation is `GET /donations` (base URL `https://donorbox.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-donations.md) for the provider-specific parameters and requirements.

