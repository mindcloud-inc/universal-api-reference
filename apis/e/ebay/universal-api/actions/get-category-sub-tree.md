# eBay: Get Category Sub-Tree

Retrieves a category Sub-Tree.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-sub-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-sub-tree?connectionId=$CONNECTION_ID&categoryTreeID=string&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryTreeID": "string",
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-sub-tree?${params}`, {
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
| `categoryTreeID` | string | yes | The unique identifier of the eBay category tree. The category tree ID for an eBay marketplace can be retrieved using the "Get Default Category Tree" action. |
| `categoryId` | string | yes | The unique identifier of the category at the top of the subtree being requested. Metadata on this category and all its descendant categories are retrieved. Note: If the category_id submitted identifies a leaf node of the tree, the call response will contain information about only that leaf node, which is a valid subtree. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categorySubtreeNode": {
        "category": {
          "categoryId": "string",
          "categoryName": "Ava Chen"
        },
        "categoryTreeNodeLevel": 1,
        "leafCategoryTreeNode": true,
        "parentCategoryTreeNodeHref": "string"
      },
      "categoryTreeId": "string",
      "categoryTreeVersion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categorySubtreeNode.category.categoryId` | string |  |
| `categorySubtreeNode.category.categoryName` | string |  |
| `categorySubtreeNode.categoryTreeNodeLevel` | number |  |
| `categorySubtreeNode.leafCategoryTreeNode` | boolean |  |
| `categorySubtreeNode.parentCategoryTreeNodeHref` | string |  |
| `categoryTreeId` | string |  |
| `categoryTreeVersion` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET commerce/taxonomy/v1/category_tree/:categoryTreeID/get_category_subtree` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-sub-tree.md) for the provider-specific parameters and requirements.

