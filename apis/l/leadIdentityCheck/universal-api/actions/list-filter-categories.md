# Lead Identity Check: List Filter Categories



```
GET https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/list-filter-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lead Identity Check `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/list-filter-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/list-filter-categories?${params}`, {
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
      "category": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Available lead filter category name. |

## Native endpoint

Through the native Lead Identity Check API, this operation is `POST /filters/categories` (base URL `https://leadidentitycheck-node.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filter-categories.md) for the provider-specific parameters and requirements.

