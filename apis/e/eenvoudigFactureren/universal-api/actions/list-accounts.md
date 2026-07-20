# EenvoudigFactureren: List Accounts

Retrieves accounts from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-accounts?${params}`, {
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
      "account_id": 1,
      "account_type": "string",
      "account_type_until": "2026-05-07T12:00:00.000Z",
      "company_name": "Ava Chen",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email_address": "ava@example.com",
      "last_login": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `account_type` | string |  |
| `account_type_until` | date |  |
| `company_name` | string |  |
| `country` | string |  |
| `created` | date |  |
| `email_address` | string |  |
| `last_login` | date |  |
| `name` | string |  |
| `number` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /accounts` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

