# AdvantShop: Get Product Properties

Retrieves product properties from AdvantShop.

```
GET https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-product-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AdvantShop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-product-properties?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/get-product-properties?${params}`, {
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
| `id` | string | yes | Product identifier from AdvantShop. |
| `type` | list | no | Optional property view type, such as inDetails or inBriefDescription. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string",
      "unit": "string",
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
| `unit` | string |  |
| `value` | string |  |

## Native endpoint

Through the native AdvantShop API, this operation is `GET /products/{id}/properties` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-properties.md) for the provider-specific parameters and requirements.

