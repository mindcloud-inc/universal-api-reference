# Odoo: List Contacts

Retrieves contacts from Odoo.

```
GET https://connect.mindcloud.co/v1/universal/odoo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Odoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/odoo/latest/actions/list-contacts?${params}`, {
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
| `domain` | string | no | Optional Odoo domain filter JSON array, for example [["is_company","=",true]]. |
| `fields` | string | no | Optional array of fields to return. |
| `limit` | number | no | Maximum number of records to return. |
| `offset` | number | no | Number of records to skip before returning results. |
| `order` | string | no | Optional Odoo order clause, for example name asc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "email": "ava@example.com",
      "id": 1,
      "is_company": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `is_company` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Odoo API, this operation is `POST /res.partner/search_read` (base URL `https://{{credentials.domain}}/json/2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

