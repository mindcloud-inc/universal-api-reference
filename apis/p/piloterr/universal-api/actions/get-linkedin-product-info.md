# Piloterr: Get LinkedIn Product Info



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-linkedin-product-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-linkedin-product-info?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-linkedin-product-info?${params}`, {
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
| `query` | string | yes | Full LinkedIn product page URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "companyUrl": "https://example.com",
      "learnMore": "string",
      "productCategory": "string",
      "productTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `companyUrl` | string |  |
| `learnMore` | string |  |
| `productCategory` | string |  |
| `productTitle` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /linkedin/product/info` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linkedin-product-info.md) for the provider-specific parameters and requirements.

