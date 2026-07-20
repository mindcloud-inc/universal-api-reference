# Column: Update Person Entity



```
PUT https://connect.mindcloud.co/v1/universal/column/latest/actions/update-person-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/column/latest/actions/update-person-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "ssn": "string",
  "dateOfBirth": "string",
  "address.line_1": "string",
  "address.city": "string",
  "address.state": "string",
  "address.postal_code": "string",
  "address.country_code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/update-person-entity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "ssn": "string",
    "dateOfBirth": "string",
    "address.line_1": "string",
    "address.city": "string",
    "address.state": "string",
    "address.postal_code": "string",
    "address.country_code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes |  |
| `firstName` | string | yes |  |
| `middleName` | string | no |  |
| `lastName` | string | yes |  |
| `ssn` | string | yes |  |
| `dateOfBirth` | string | yes |  |
| `address.line_1` | string | yes |  |
| `address.city` | string | yes |  |
| `address.state` | string | yes |  |
| `address.postal_code` | string | yes |  |
| `address.country_code` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `PATCH /entities/person/:entity_id` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person-entity.md) for the provider-specific parameters and requirements.

