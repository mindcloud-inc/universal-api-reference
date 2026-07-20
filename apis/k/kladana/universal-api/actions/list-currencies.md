# Kladana: List Currencies

Lists currencies in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-currencies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-currencies?${params}`, {
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
      "archived": true,
      "code": "string",
      "default": true,
      "fullName": "Ava Chen",
      "id": "string",
      "indirect": true,
      "isoCode": "string",
      "meta": {},
      "multiplicity": 1,
      "name": "Ava Chen",
      "rate": 1,
      "system": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the currency is archived. |
| `code` | string | Currency code. |
| `default` | boolean | Whether this is the default currency. |
| `fullName` | string | Full currency name. |
| `id` | string | Currency UUID. |
| `indirect` | boolean | Whether the rate is indirect. |
| `isoCode` | string | ISO currency code. |
| `meta` | object | Kladana metadata reference. |
| `multiplicity` | number | Currency multiplicity. |
| `name` | string | Currency name. |
| `rate` | number | Currency rate. |
| `system` | boolean | Whether the currency is system-defined. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/currency/` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

