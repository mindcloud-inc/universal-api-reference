# Rijksmuseum: Get Latest IIIF Change Discovery Page



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-latest-iiif-change-discovery-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-latest-iiif-change-discovery-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-latest-iiif-change-discovery-page?${params}`, {
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
      "@context": "string",
      "id": "string",
      "orderedItems": [
        {}
      ],
      "partOf": {},
      "prev": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `id` | string |  |
| `orderedItems` | array<object> |  |
| `partOf` | object |  |
| `prev` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /cd/pages/last.json` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-iiif-change-discovery-page.md) for the provider-specific parameters and requirements.

