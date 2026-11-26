# eBay: Get Category Tree

Retrieves a complete category tree by its ID.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-tree?connectionId=$CONNECTION_ID&categoryTreeID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryTreeID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-category-tree?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryTreeId": "string",
      "categoryTreeVersion": "string",
      "rootCategoryNode": {
        "category": {
          "categoryId": "string",
          "categoryName": "Ava Chen"
        },
        "categoryTreeNodeLevel": 1,
        "childCategoryTreeNodes": [
          {
            "category": {
              "categoryId": "string",
              "categoryName": "Ava Chen"
            },
            "categoryTreeNodeLevel": 1,
            "childCategoryTreeNodes": [
              {
                "category": {
                  "categoryId": "string",
                  "categoryName": "Ava Chen"
                },
                "categoryTreeNodeLevel": 1,
                "childCategoryTreeNodes": [
                  {
                    "category": {
                      "categoryId": "string",
                      "categoryName": "Ava Chen"
                    },
                    "categoryTreeNodeLevel": 1,
                    "childCategoryTreeNodes": [
                      {
                        "category": {
                          "categoryId": "string",
                          "categoryName": "Ava Chen"
                        },
                        "categoryTreeNodeLevel": 1,
                        "leafCategoryTreeNode": true,
                        "parentCategoryTreeNodeHref": "string"
                      }
                    ],
                    "parentCategoryTreeNodeHref": "string"
                  }
                ],
                "parentCategoryTreeNodeHref": "string"
              }
            ],
            "parentCategoryTreeNodeHref": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryTreeId` | string |  |
| `categoryTreeVersion` | string |  |
| `rootCategoryNode.category.categoryId` | string |  |
| `rootCategoryNode.category.categoryName` | string |  |
| `rootCategoryNode.categoryTreeNodeLevel` | number |  |
| `rootCategoryNode.childCategoryTreeNodes[].category.categoryId` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].category.categoryName` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].categoryTreeNodeLevel` | number |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryId` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryName` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].categoryTreeNodeLevel` | number |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryId` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryName` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].categoryTreeNodeLevel` | number |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryId` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].category.categoryName` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].categoryTreeNodeLevel` | number |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].leafCategoryTreeNode` | boolean |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].parentCategoryTreeNodeHref` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].childCategoryTreeNodes[].parentCategoryTreeNodeHref` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].childCategoryTreeNodes[].parentCategoryTreeNodeHref` | string |  |
| `rootCategoryNode.childCategoryTreeNodes[].parentCategoryTreeNodeHref` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET commerce/taxonomy/v1/category_tree/:categoryTreeID` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-tree.md) for the provider-specific parameters and requirements.

