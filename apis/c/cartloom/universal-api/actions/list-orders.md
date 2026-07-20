# Cartloom: List Orders

Retrieves multiple order records from Cartloom.

```
GET https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cartloom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-orders?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/list-orders?${params}`, {
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
| `startDate` | date | yes | Start date in YYYY-MM-DD format. |
| `endDate` | date | yes | End date in YYYY-MM-DD format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchType` | list | no | Search type, either email or last_name. One of: `0`, `1`. |
| `keyword` | string | no | Keyword value for the selected search type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "invoice": "string",
      "status": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Order date. |
| `email` | string | Customer email address. |
| `invoice` | string | Order invoice number. |
| `status` | string | Order status. |
| `total` | string | Order total. |

## Native endpoint

Through the native Cartloom API, this operation is `POST /orders/list/format/json` (base URL `https://mindcloudstage0424.cartloom.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

