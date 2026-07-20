# TravelPerk: List Invoice Lines

Retrieves invoice lines from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-invoice-lines?${params}`, {
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
| `expenseDateGte` | string | no | Return invoice lines with an expense date on or after this date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `expenseDateLte` | string | no | Return invoice lines with an expense date on or before this date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoice_lines": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoice_lines` | array<object> |  |
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /invoices/lines` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoice-lines.md) for the provider-specific parameters and requirements.

