# Printify: List Blueprint Print Providers

Retrieves blueprint print providers from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-print-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-print-providers?connectionId=$CONNECTION_ID&blueprintId=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintId": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprint-print-providers?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "decorationMethods": [
        "string"
      ],
      "id": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `decorationMethods` | array<string> |  |
| `id` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Printify API, this operation is `GET /catalog/blueprints/:blueprint_id/print_providers.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blueprint-print-providers.md) for the provider-specific parameters and requirements.

