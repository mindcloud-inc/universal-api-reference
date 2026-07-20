# Gumroad: Update Custom Field

Updates an existing custom field in Gumroad.

```
PUT https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/update-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | The product ID. |
| `name` | string | yes | The custom field name. |
| `required` | boolean | no | Whether the custom field is required. |
| `variant` | string | no | The variant this custom field applies to, when applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customField": {
        "name": "Ava Chen",
        "required": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customField` | object |  |
| `customField.name` | string |  |
| `customField.required` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `PUT /products/:product_id/custom_fields/:name` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-field.md) for the provider-specific parameters and requirements.

