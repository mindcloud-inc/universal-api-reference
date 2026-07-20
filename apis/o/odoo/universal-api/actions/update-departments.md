# Odoo: Update Departments

Updates existing departments in Odoo.

```
PUT https://connect.mindcloud.co/v1/universal/odoo/latest/actions/update-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Odoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/odoo/latest/actions/update-departments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    1
  ],
  "vals": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/odoo/latest/actions/update-departments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": [1],
    "vals": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<number> | yes | Array of Odoo department IDs to update as JSON. |
| `vals` | object | yes | Object of department fields and values to update as JSON. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Odoo API, this operation is `POST /hr.department/write` (base URL `https://{{credentials.domain}}/json/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-departments.md) for the provider-specific parameters and requirements.

