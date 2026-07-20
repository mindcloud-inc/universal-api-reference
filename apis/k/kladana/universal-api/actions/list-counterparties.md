# Kladana: List Counterparties

Lists counterparties in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-counterparties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-counterparties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-counterparties?${params}`, {
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
      "accounts": [
        {}
      ],
      "actualAddress": "string",
      "archived": true,
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalCode": "string",
      "group": {},
      "id": "string",
      "inn": "string",
      "kpp": "string",
      "legalTitle": "string",
      "meta": {},
      "name": "Ava Chen",
      "ogrn": "string",
      "owner": {},
      "phone": "string",
      "shared": true,
      "tags": [
        "string"
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
| `accounts` | array<object> | Bank accounts. |
| `actualAddress` | string | Actual address. |
| `archived` | boolean | Whether the counterparty is archived. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `email` | string | Email address. |
| `externalCode` | string | External code. |
| `group` | object | Group reference. |
| `id` | string | Counterparty UUID. |
| `inn` | string | Taxpayer identifier. |
| `kpp` | string | Tax registration reason code. |
| `legalTitle` | string | Legal title. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Counterparty name. |
| `ogrn` | string | Registration number. |
| `owner` | object | Owner reference. |
| `phone` | string | Phone number. |
| `shared` | boolean | Whether the counterparty is shared. |
| `tags` | array<string> | Counterparty tags. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/counterparty` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-counterparties.md) for the provider-specific parameters and requirements.

