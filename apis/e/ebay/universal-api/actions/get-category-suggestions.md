# eBay: Get Category Suggestions

Retrieve a categories that are considered by eBay to most closely correspond to the provided query.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-suggestions?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-suggestions?${params}`, {
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
| `q` | string | yes | A quoted string that describes or characterizes the item being offered for sale. The string format is free form, and can contain any combination of phrases or keywords. eBay will parse the string and return suggested categories for the item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {
        "categoryId": "string",
        "categoryName": "Ava Chen"
      },
      "categoryTreeNodeAncestors": [
        {
          "categoryId": "string",
          "categoryName": "Ava Chen",
          "categorySubtreeNodeHref": "string",
          "categoryTreeNodeLevel": 1
        }
      ],
      "categoryTreeNodeLevel": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category.categoryId` | string |  |
| `category.categoryName` | string |  |
| `categoryTreeNodeAncestors[].categoryId` | string |  |
| `categoryTreeNodeAncestors[].categoryName` | string |  |
| `categoryTreeNodeAncestors[].categorySubtreeNodeHref` | string |  |
| `categoryTreeNodeAncestors[].categoryTreeNodeLevel` | number |  |
| `categoryTreeNodeLevel` | number |  |

## Native endpoint

Through the native eBay API, this operation is `GET commerce/taxonomy/v1/category_tree/0/get_category_suggestions` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-suggestions.md) for the provider-specific parameters and requirements.

