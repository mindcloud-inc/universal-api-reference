# eBay: Get Default Category Tree



```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-default-category-tree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-default-category-tree?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-default-category-tree?${params}`, {
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
| `marketplaceID` | string | no | The unique identifier of the eBay marketplace for which the category tree ID is requested. For a list of supported marketplace IDs, see Marketplaces with Default Category Trees. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `categoryTreeId` | string |  |
| `categoryTreeVersion` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET commerce/taxonomy/v1/get_default_category_tree_id` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-category-tree.md) for the provider-specific parameters and requirements.

