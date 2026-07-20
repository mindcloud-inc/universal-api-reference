# smapOne: Get category smaps

Retrieves smaps in a category from smapOne.

```
GET https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-category-smaps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-category-smaps?connectionId=$CONNECTION_ID&category_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/get-category-smaps?${params}`, {
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
| `category_id` | string | yes | The category id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "smapId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `smapId` | string |  |
| `title` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `GET /smaps/overview/categories/{categoryId}` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-smaps.md) for the provider-specific parameters and requirements.

