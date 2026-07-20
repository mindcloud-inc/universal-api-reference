# Level: Update Custom Field

Updates an existing custom field in Level.

```
PUT https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the custom field. |
| `name` | string | no | The updated name of the custom field. |
| `adminOnly` | boolean | no | Whether only administrators can view or edit this field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminOnly": true,
      "id": "string",
      "name": "Ava Chen",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminOnly` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |

## Native endpoint

Through the native Level API, this operation is `PATCH /custom_fields/{id}` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field.md) for the provider-specific parameters and requirements.

