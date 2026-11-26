# eBay: List Item Aspects for Category

Returns a complete list of aspects for all of the leaf categories that belong to an eBay marketplace.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-item-aspects-for-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-item-aspects-for-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-item-aspects-for-category?${params}`, {
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
| `categoryId` | string | yes | The unique identifier of the leaf category for which aspects are being requested. |

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

Through the native eBay API, this operation is `GET commerce/taxonomy/v1/category_tree/0/get_item_aspects_for_category` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-aspects-for-category.md) for the provider-specific parameters and requirements.

