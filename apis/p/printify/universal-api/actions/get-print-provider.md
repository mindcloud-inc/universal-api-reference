# Printify: Get Print Provider

Retrieves a print provider from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-print-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-print-provider?connectionId=$CONNECTION_ID&printProviderId=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "printProviderId": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-print-provider?${params}`, {
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
| `printProviderId` | number | yes | Printify print provider id. Default: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprints": [
        {}
      ],
      "id": 1,
      "location": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprints` | array<object> |  |
| `id` | number |  |
| `location` | object |  |
| `title` | string |  |

## Native endpoint

Through the native Printify API, this operation is `GET /catalog/print_providers/:print_provider_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-provider.md) for the provider-specific parameters and requirements.

