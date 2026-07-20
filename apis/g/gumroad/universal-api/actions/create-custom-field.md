# Gumroad: Create Custom Field

Creates a new custom field in Gumroad.

```
POST https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen",
  "required": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "name": "Ava Chen",
    "required": true
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
| `required` | boolean | yes | Whether the custom field is required. |
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

Through the native Gumroad API, this operation is `POST /products/:product_id/custom_fields` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

