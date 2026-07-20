# Gelato: List Catalogs

Finds available product catalogs in Gelato.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs?${params}`, {
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
      "catalogUid": "string",
      "productAttributes": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogUid` | string | Gelato catalog identifier. |
| `productAttributes` | array<object> | Available product attribute definitions for the catalog. |
| `title` | string | Catalog title. |

## Native endpoint

Through the native Gelato API, this operation is `GET https://product.gelatoapis.com/v3/catalogs` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-catalogs.md) for the provider-specific parameters and requirements.

