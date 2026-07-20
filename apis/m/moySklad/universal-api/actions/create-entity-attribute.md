# MoySklad: Create entity attribute

Creates an entity attribute in MoySklad.

```
POST https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-entity-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-entity-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "product",
  "name": "MindCloud Validator Attribute",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/create-entity-attribute', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "product",
    "name": "MindCloud Validator Attribute",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | MoySklad entity type. Default: `product`. |
| `name` | string | yes | MoySklad name argument. Default: `MindCloud Validator Attribute`. |
| `required` | boolean | no | MoySklad required argument. Default: `false`. |
| `type` | string | yes | MoySklad type argument. Default: `string`. |

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

Through the native MoySklad API, this operation is `POST entity/:entityType/metadata/attributes` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-entity-attribute.md) for the provider-specific parameters and requirements.

