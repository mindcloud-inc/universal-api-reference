# Kladana: List Organizations

Lists organizations in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-organizations?${params}`, {
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
      "id": "string",
      "inn": "string",
      "kpp": "string",
      "legalAddress": "string",
      "legalTitle": "string",
      "meta": {},
      "name": "Ava Chen",
      "ogrn": "string",
      "phone": "string",
      "shared": true,
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
| `archived` | boolean | Whether the organization is archived. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `email` | string | Email address. |
| `externalCode` | string | External code. |
| `id` | string | Organization UUID. |
| `inn` | string | Taxpayer identifier. |
| `kpp` | string | Tax registration reason code. |
| `legalAddress` | string | Legal address. |
| `legalTitle` | string | Legal title. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Organization name. |
| `ogrn` | string | Registration number. |
| `phone` | string | Phone number. |
| `shared` | boolean | Whether the organization is shared. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/organization` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

