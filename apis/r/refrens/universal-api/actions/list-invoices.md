# Refrens: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refrens/latest/actions/list-invoices?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortCreatedAt` | number | no | Set to 1 for ascending or -1 for descending. |
| `sortInvoiceNumber` | number | no | Set to 1 for ascending or -1 for descending. |
| `sortInvoiceDate` | number | no | Set to 1 for ascending or -1 for descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "limit": 1,
      "skip": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | number |  |
| `skip` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Refrens API, this operation is `GET /businesses/:urlKey/invoices` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

