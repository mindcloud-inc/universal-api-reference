# Bexio: List Bills

Retrieves bills from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-bills?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-bills?${params}`, {
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
| `limit` | number | no | Limit the number of results (max is 500). |
| `page` | number | no | Current page. |
| `order` | list<string> | no | Sorting order. One of: `0`, `1`. |
| `sort` | string | no | Field to sort by. |
| `fields[]` | array<string> | no | Fields for which search will be run. |
| `searchTerm` | string | no | Term to search for. Minimum 3 characters, maximum 255 characters. |
| `status` | list<string> | no | Bill status filter. One of: `0`, `1`, `2`, `3`. |
| `billDateStart` | date | no | Earliest accepted bill date. |
| `billDateEnd` | date | no | Latest accepted bill date. |
| `dueDateStart` | date | no | Earliest accepted due date. |
| `dueDateEnd` | date | no | Latest accepted due date. |
| `vendorRef` | string | no | Filter for vendor reference. |
| `title` | string | no | Filter by bill title. |
| `currencyCode` | string | no | Filter by currency code. |
| `pendingAmountMin` | number | no | Minimum pending amount. |
| `pendingAmountMax` | number | no | Maximum pending amount. |
| `vendor` | string | no | Vendor filter. |
| `grossMin` | number | no | Minimum gross amount. |
| `grossMax` | number | no | Maximum gross amount. |
| `netMin` | number | no | Minimum net amount. |
| `netMax` | number | no | Maximum net amount. |
| `documentNo` | string | no | Filter by document number. |
| `supplierId` | number | no | Filter by supplier ID. |
| `averageExchangeRateEnabled` | boolean | no | Filter by average exchange rate flag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {
        "itemCount": 1,
        "page": 1,
        "pageCount": 1,
        "pageSize": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paging.itemCount` | number |  |
| `paging.page` | number |  |
| `paging.pageCount` | number |  |
| `paging.pageSize` | number |  |

## Native endpoint

Through the native Bexio API, this operation is `GET /4.0/purchase/bills` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

