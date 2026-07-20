# Bexio: List Expenses

Retrieves expenses from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-expenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/list-expenses?${params}`, {
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
| `limit` | number | no |  |
| `page` | number | no |  |
| `order` | list<string> | no | One of: `0`, `1`. |
| `sort` | string | no |  |
| `vendor` | string | no |  |
| `grossMin` | number | no |  |
| `grossMax` | number | no |  |
| `netMin` | number | no |  |
| `netMax` | number | no |  |
| `paidOnStart` | date | no |  |
| `paidOnEnd` | date | no |  |
| `createdAtStart` | date | no |  |
| `createdAtEnd` | date | no |  |
| `title` | string | no |  |
| `currencyCode` | string | no |  |
| `documentNo` | string | no |  |
| `supplierId` | number | no |  |
| `projectId` | string | no |  |

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

Through the native Bexio API, this operation is `GET /4.0/expenses` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expenses.md) for the provider-specific parameters and requirements.

