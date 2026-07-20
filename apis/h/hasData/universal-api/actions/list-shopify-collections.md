# HasData: List Shopify Collections

Retrieves Shopify collections from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-collections?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-collections?${params}`, {
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
| `limit` | number | no | Maximum number of collections to retrieve. |
| `page` | number | no | Page number of collection results. |
| `url` | string | yes | Shopify store URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collections": [
        {}
      ],
      "requestMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collections` | array<object> |  |
| `requestMetadata` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/shopify/collections` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shopify-collections.md) for the provider-specific parameters and requirements.

