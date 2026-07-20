# Odoo: Get Departments By IDs

Retrieves departments by ID from Odoo.

```
GET https://connect.mindcloud.co/v1/universal/odoo/latest/actions/get-departments-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Odoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/get-departments-by-ids?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/odoo/latest/actions/get-departments-by-ids?${params}`, {
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
| `fields[]` | array<string> | no | Optional array of department field names to include. |
| `ids[]` | array<number> | yes | Array of Odoo department IDs to read as JSON. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Odoo API, this operation is `POST /hr.department/read` (base URL `https://{{credentials.domain}}/json/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-departments-by-ids.md) for the provider-specific parameters and requirements.

