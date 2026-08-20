# Centerpoint: List Product Template Tags



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-product-template-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-product-template-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-product-template-tags?${params}`, {
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
      "attributes": {
        "accountId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "domain": "string",
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.domain` | string |  |
| `attributes.name` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET product_template_tags` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-template-tags.md) for the provider-specific parameters and requirements.

