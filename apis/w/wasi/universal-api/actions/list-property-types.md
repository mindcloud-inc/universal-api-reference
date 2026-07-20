# Wasi: List Property Types

Retrieves property types from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-types?${params}`, {
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
| `for_rent` | boolean | no | Only count rental inventory. |
| `for_sale` | boolean | no | Only count sale inventory. |
| `for_transfer` | boolean | no | Only count transfer inventory. |
| `quantity` | boolean | no | Include the number of matching properties per property type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_property_type": 1,
      "name": "Ava Chen",
      "nombre": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_property_type` | number | Wasi property type identifier. |
| `name` | string | Property type name. |
| `nombre` | string | Localized property type label from Wasi. |

## Native endpoint

Through the native Wasi API, this operation is `GET /property-type/all` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-property-types.md) for the provider-specific parameters and requirements.

