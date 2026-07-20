# MoySklad: Update entity attribute

Updates an entity attribute in MoySklad.

```
PUT https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/update-entity-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/update-entity-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributeId": "91121e74-3ce8-11f1-0a80-07ab0001c357",
  "body": {
    "name": "MindCloud Validator Attribute",
    "required": false
  },
  "entityType": "product"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/update-entity-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributeId": "91121e74-3ce8-11f1-0a80-07ab0001c357",
    "body": {"name":"MindCloud Validator Attribute","required":false},
    "entityType": "product"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributeId` | string | yes | MoySklad attribute ID. Default: `91121e74-3ce8-11f1-0a80-07ab0001c357`. |
| `body` | object | yes | Attribute update payload. Default: `{"name":"MindCloud Validator Attribute","required":false}`. |
| `entityType` | string | yes | MoySklad entity type. Default: `product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `meta` | object |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native MoySklad API, this operation is `PUT entity/:entityType/metadata/attributes/:attributeId` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-entity-attribute.md) for the provider-specific parameters and requirements.

