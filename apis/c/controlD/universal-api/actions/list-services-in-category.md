# Control D: List Services In Category

Retrieves services in a category from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-services-in-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-services-in-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-services-in-category?${params}`, {
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
| `category` | string | yes | Category name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "locations": [
        "string"
      ],
      "name": "Ava Chen",
      "PK": "string",
      "unlock_location": "string",
      "warning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `locations` | array<string> |  |
| `name` | string |  |
| `PK` | string |  |
| `unlock_location` | string |  |
| `warning` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /services/categories/:category` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services-in-category.md) for the provider-specific parameters and requirements.

