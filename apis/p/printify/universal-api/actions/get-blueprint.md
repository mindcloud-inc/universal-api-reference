# Printify: Get Blueprint

Retrieves a blueprint from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint?connectionId=$CONNECTION_ID&blueprint_id=5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprint_id": "5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-blueprint?${params}`, {
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
| `blueprint_id` | number | yes | Printify blueprint id. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": "string",
      "description": "string",
      "id": 1,
      "model": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | string |  |
| `description` | string |  |
| `id` | number |  |
| `model` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Printify API, this operation is `GET /catalog/blueprints/:blueprint_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blueprint.md) for the provider-specific parameters and requirements.

