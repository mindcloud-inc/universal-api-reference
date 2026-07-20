# Level: Update Custom Field Value

Updates a custom field value in Level.

```
PUT https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFieldId": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/level/latest/actions/update-custom-field-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFieldId": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldId` | string | yes | The ID of the custom field to set the value for. |
| `assignedToId` | string | no | The ID of the device or group to assign the value to. |
| `value` | string | yes | The custom field value to set. |
| `force` | boolean | no | Whether to override descendant values when setting this custom field value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToId": "string",
      "customFieldId": "string",
      "customFieldName": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToId` | string |  |
| `customFieldId` | string |  |
| `customFieldName` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Level API, this operation is `PATCH /custom_field_values` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field-value.md) for the provider-specific parameters and requirements.

