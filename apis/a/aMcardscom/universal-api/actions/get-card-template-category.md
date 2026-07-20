# AMcards.com: Get Card Template Category

Retrieves a specific card template category from AMcards.com.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-card-template-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-card-template-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/get-card-template-category?${params}`, {
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
| `categoryId` | number | no | AMcards category identifier from the `/category/` resource URI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "parent": "string",
      "priority": 1,
      "resourceUri": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `parent` | string |  |
| `priority` | number |  |
| `resourceUri` | string |  |
| `title` | string |  |

## Native endpoint

Through the native AMcards.com API, this operation is `GET /category/:categoryId/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-template-category.md) for the provider-specific parameters and requirements.

