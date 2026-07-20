# Zydon: Get Price Table

Retrieves price table details from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-price-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-price-table?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-price-table?${params}`, {
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
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "start_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end_date` | date | Price table end date. |
| `id` | string | Price table identifier. |
| `name` | string | Price table name. |
| `start_date` | date | Price table start date. |

## Native endpoint

Through the native Zydon API, this operation is `GET /price-tables/{id}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-price-table.md) for the provider-specific parameters and requirements.

