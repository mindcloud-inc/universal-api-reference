# Webshipper: Update Return Shipping Method

Updates a return shipping method in Webshipper.

```
PUT https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-shipping-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-shipping-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/update-return-shipping-method', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The return shipping method ID. |
| `data.id` | string | yes | Repeat the ID value for the JSON:API request body. |
| `data.attributes.name` | string | no | Updated return shipping method name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "excluded_countries": [
        "string"
      ],
      "excluded_skus": [
        "string"
      ],
      "excluded_zip_codes": [
        "string"
      ],
      "id": "string",
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
| `excluded_countries` | array<string> |  |
| `excluded_skus` | array<string> |  |
| `excluded_zip_codes` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `PATCH /return_shipping_methods/:id` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-return-shipping-method.md) for the provider-specific parameters and requirements.

