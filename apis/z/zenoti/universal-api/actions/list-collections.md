# Zenoti: Get Collections Report



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-collections?${params}`, {
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
| `centers.ids[]` | array<object> | no |  |
| `centers.ids[].center` | list | no |  |
| `invoiceStatuses[].invoiceStatus` | list | no |  |
| `paymentTypes[].paymentType` | list | no |  |
| `saleTypes[].salesType` | list | no |  |
| `startDate` | date | no |  |
| `centers.allCenters` | boolean | no | Default: `false`. |
| `centers.reportType` | list | no |  |
| `endDate` | date | no |  |
| `centers` | object | no |  |
| `paymentTypes[]` | array | no |  |
| `saleTypes[]` | array<object> | no |  |
| `invoiceStatuses[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zenoti API returns.

## Native endpoint

Through the native Zenoti API, this operation is `POST reports/collections/flat_file` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

