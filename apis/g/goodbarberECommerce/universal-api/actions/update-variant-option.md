# Goodbarber eCommerce: Update Variant Option



```
PUT https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-variant-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-variant-option" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "optionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/update-variant-option', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "optionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optionId` | number | yes | Variant option ID. |
| `name` | string | no | Updated variant option display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "string",
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `id` | number | Variant option ID. |
| `name` | string | Variant option name. |
| `updatedAt` | string | Last update timestamp. |
| `values` | array<object> | Option values. |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `PATCH /publicapi/v2/general/catalog/:webzine_id/option/:option_id/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-variant-option.md) for the provider-specific parameters and requirements.

