# Quentn: Create Custom Field



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "MindCloud Stage 2 Field",
  "fieldType": "text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "MindCloud Stage 2 Field",
    "fieldType": "text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | Visible label of the custom field. Example: `MindCloud Stage 2 Field`. |
| `fieldType` | string | yes | Custom field type such as text, selection, date, integer, float, checkbox_confirmation, or url. Example: `text`. |
| `description` | string | no | Optional description shown for the custom field. Example: `Created during Quentn validation`. |
| `fieldName` | string | no | Optional unique identifier. Quentn prefixes it with field_ automatically. Example: `mindcloud_stage2_field`. |
| `maxLength` | number | no | Optional max length for text fields. Allowed values include 8, 16, 32, 64, 128, and 255. Example: `255`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldId": "string",
      "fieldName": "Ava Chen",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldId` | string | The id of the created Quentn custom field. |
| `fieldName` | string | The machine name Quentn assigned to the created custom field. |
| `success` | boolean | Whether Quentn accepted the custom field create request. |

## Native endpoint

Through the native Quentn API, this operation is `POST /custom-fields` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

