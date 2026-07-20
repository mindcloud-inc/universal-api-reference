# Printify: List Blueprints

Retrieves blueprints from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-blueprints?${params}`, {
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
| `limit` | number | no | Maximum number of blueprints to return. |
| `page` | number | no | Result page to fetch. |

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

Through the native Printify API, this operation is `GET /catalog/blueprints.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blueprints.md) for the provider-specific parameters and requirements.

