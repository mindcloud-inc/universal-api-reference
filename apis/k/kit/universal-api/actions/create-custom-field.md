# Kit: Create Custom Field

Creates a new custom field in Kit.

```
POST https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Unique custom field label to create in Kit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_field": {
        "id": 1,
        "key": "string",
        "label": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_field` | object | Created custom field. |
| `custom_field.id` | number | Custom field ID. |
| `custom_field.key` | string | Custom field key used in subscriber field payloads. |
| `custom_field.label` | string | Human-readable custom field label. |
| `custom_field.name` | string | Generated custom field name. |

## Native endpoint

Through the native Kit API, this operation is `POST /custom_fields` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

