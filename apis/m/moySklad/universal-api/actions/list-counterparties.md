# MoySklad: List counterparties

Retrieves counterparties from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-counterparties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-counterparties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/list-counterparties?${params}`, {
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
      "code": "string",
      "context": {},
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "rows": [
        {}
      ],
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `context` | object |  |
| `externalCode` | string |  |
| `id` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `rows` | array<object> |  |
| `updated` | date |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET entity/counterparty` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-counterparties.md) for the provider-specific parameters and requirements.

