# respond.io: Create Custom Field

Creates a new custom field in respond.io.

```
POST https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataType": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataType": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedValues` | string | no | Allowed values for select-type fields. |
| `dataType` | string | yes | Custom field data type. |
| `description` | string | no | Custom field description. |
| `name` | string | yes | Custom field name. |
| `slug` | string | no | Unique custom field slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "dataType": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /space/custom_field` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

