# Quizell: Create Customer Custom Field

Creates a customer custom field in Quizell.

```
POST https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldName": "Ava Chen",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-customer-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldName": "Ava Chen",
    "fieldType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldName` | string | yes | Name or label of the custom field. |
| `fieldType` | string | yes | Type of field (text, textarea, select, checkbox, radio). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_name": "Ava Chen",
      "field_type": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_name` | string |  |
| `field_type` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Quizell API, this operation is `POST /customers/custom_fields/store` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-custom-field.md) for the provider-specific parameters and requirements.

