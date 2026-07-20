# MoySklad: Delete entity attribute

Deletes an entity attribute from MoySklad.

```
DELETE https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-entity-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-entity-attribute?connectionId=$CONNECTION_ID&attributeId=91121e74-3ce8-11f1-0a80-07ab0001c357&entityType=product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attributeId": "91121e74-3ce8-11f1-0a80-07ab0001c357",
  "entityType": "product"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/delete-entity-attribute?${params}`, {
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
| `attributeId` | string | yes | MoySklad attribute ID. Default: `91121e74-3ce8-11f1-0a80-07ab0001c357`. |
| `entityType` | string | yes | MoySklad entity type. Default: `product`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "meta": {},
      "success": true
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
| `success` | boolean |  |

## Native endpoint

Through the native MoySklad API, this operation is `DELETE entity/:entityType/metadata/attributes/:attributeId` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entity-attribute.md) for the provider-specific parameters and requirements.

