# Reloadify: Create Or Update Custom Attribute

Creates or updates a custom attribute in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-custom-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-custom-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "custom_attribute.name": "Ava Chen",
  "custom_attribute.description": "string",
  "custom_attribute.datatype": "string",
  "custom_attribute.resource": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-custom-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "custom_attribute.name": "Ava Chen",
    "custom_attribute.description": "string",
    "custom_attribute.datatype": "string",
    "custom_attribute.resource": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom_attribute.name` | string | yes | Custom attribute name. |
| `custom_attribute.description` | string | yes | Custom attribute description. |
| `custom_attribute.datatype` | string | yes | Datatype: string, integer, float, or boolean. |
| `custom_attribute.resource` | string | yes | Resource: profile, product, order, shopping_cart, category, review, variant, or brand. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datatype": "string",
      "description": "string",
      "handle": "string",
      "name": "Ava Chen",
      "resource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datatype` | string |  |
| `description` | string |  |
| `handle` | string |  |
| `name` | string |  |
| `resource` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/custom_attributes` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-custom-attribute.md) for the provider-specific parameters and requirements.

