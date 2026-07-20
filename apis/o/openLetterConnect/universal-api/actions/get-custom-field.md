# Open Letter Connect: Get Custom Field

Retrieves a custom field from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-custom-field?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-custom-field?${params}`, {
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

Through the native Open Letter Connect API, this operation is `GET /custom-fields/:id` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-field.md) for the provider-specific parameters and requirements.

