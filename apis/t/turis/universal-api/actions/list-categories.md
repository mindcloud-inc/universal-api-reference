# Turis: List Categories

Retrieves categories from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryName": "Ava Chen",
      "categorySlug": "string",
      "id": 1,
      "isVisible": 1,
      "nested": [
        {
          "categoryName": "Ava Chen",
          "categorySlug": "string",
          "id": 1,
          "parentId": 1
        }
      ],
      "parentId": 1,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryName` | string |  |
| `categorySlug` | string |  |
| `id` | number |  |
| `isVisible` | number |  |
| `nested[].categoryName` | string |  |
| `nested[].categorySlug` | string |  |
| `nested[].id` | number |  |
| `nested[].parentId` | number |  |
| `parentId` | number |  |
| `position` | number |  |

## Native endpoint

Through the native Turis API, this operation is `GET /api/public/v1/categories` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

