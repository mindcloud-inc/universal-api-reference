# Open Letter Connect: Update Custom Field

Updates a custom field in Open Letter Connect.

```
PUT https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/update-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/update-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFieldName": "Ava Chen",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/update-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFieldName": "Ava Chen",
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldName` | string | yes | The custom field label to save. |
| `id` | number | yes | The numeric custom field ID from Open Letter Connect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customFieldCategoryId": "string",
      "defaultValue": "string",
      "id": "string",
      "isLiveMode": true,
      "key": "string",
      "sortOrder": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `customFieldCategoryId` | string |  |
| `defaultValue` | string |  |
| `id` | string |  |
| `isLiveMode` | boolean |  |
| `key` | string |  |
| `sortOrder` | number |  |
| `value` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `PUT /custom-fields/:id` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field.md) for the provider-specific parameters and requirements.

