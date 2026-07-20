# Nyckel: Update Field

Updates an existing field in Nyckel.

```
PUT https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "fieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "fieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Nyckel function identifier. |
| `fieldId` | string | yes | Nyckel field identifier. |
| `name` | string | no | Updated field name. |
| `type` | string | no | Updated field type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Nyckel field ID. |
| `name` | string | Field name. |
| `type` | string | Field type. |

## Native endpoint

Through the native Nyckel API, this operation is `PUT /functions/:functionId/fields/:fieldId` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

