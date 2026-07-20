# Landbot: Create Customer Field

Creates a customer field in Landbot.

```
POST https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-customer-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-customer-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "fieldName": "Ava Chen",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landbot/latest/actions/create-customer-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "fieldName": "Ava Chen",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Customer ID that owns the field. |
| `fieldName` | string | yes | Field name to create on the customer. |
| `type` | string | no | Optional field type. Allowed values: string, integer, float, boolean, date, datetime. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extra` | object | no | Optional extra field metadata object. |
| `value` | string | yes | Field value. Landbot accepts a value matching the selected type; this field is required. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Landbot API, this operation is `POST /v1/customers/:customer_id/fields/:field_name/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-field.md) for the provider-specific parameters and requirements.

