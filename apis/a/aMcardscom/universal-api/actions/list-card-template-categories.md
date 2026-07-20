# AMcards.com: List Card Template Categories

Retrieves card template categories from AMcards.com.

```
GET https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-card-template-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AMcards.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-card-template-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-card-template-categories?${params}`, {
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
| `parentId` | number | no | Filter categories by parent category ID. |
| `parentTitleContains` | string | no | Filter categories by partial parent-title match. |
| `titleContains` | string | no | Filter categories by partial title match. |

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

Through the native AMcards.com API, this operation is `GET /category/` (base URL `https://amcards.com/.api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-card-template-categories.md) for the provider-specific parameters and requirements.

