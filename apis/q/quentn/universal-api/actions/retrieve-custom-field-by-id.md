# Quentn: Retrieve Custom Field by ID



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-custom-field-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-custom-field-by-id?connectionId=$CONNECTION_ID&field_id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field_id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/retrieve-custom-field-by-id?${params}`, {
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
| `field_id` | number | yes | The numeric Quentn custom field id to retrieve. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultValue": "string",
      "description": "string",
      "fieldId": "string",
      "fieldName": "Ava Chen",
      "fieldType": "string",
      "label": "string",
      "multipleSelection": true,
      "required": true,
      "settings": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultValue` | string |  |
| `description` | string |  |
| `fieldId` | string |  |
| `fieldName` | string |  |
| `fieldType` | string |  |
| `label` | string |  |
| `multipleSelection` | boolean |  |
| `required` | boolean |  |
| `settings` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Quentn API, this operation is `GET /custom-fields/:field_id` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-custom-field-by-id.md) for the provider-specific parameters and requirements.

