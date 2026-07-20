# Printify: List Blueprint Variants

Retrieves blueprint variants from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-variants?connectionId=$CONNECTION_ID&blueprintId=5&printProviderId=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintId": "5",
  "printProviderId": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-variants?${params}`, {
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
| `blueprintId` | number | yes | Printify blueprint id. Default: `5`. |
| `printProviderId` | number | yes | Printify print provider id. Default: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "title": "string",
      "variants": [
        {
          "id": 1,
          "isEnabled": true,
          "price": 1,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `title` | string |  |
| `variants` | array<object> |  |
| `variants[].id` | number |  |
| `variants[].isEnabled` | boolean |  |
| `variants[].price` | number |  |
| `variants[].title` | string |  |

## Native endpoint

Through the native Printify API, this operation is `GET /catalog/blueprints/:blueprint_id/print_providers/:print_provider_id/variants.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blueprint-variants.md) for the provider-specific parameters and requirements.

