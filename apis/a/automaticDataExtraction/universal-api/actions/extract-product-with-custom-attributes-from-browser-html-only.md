# Automatic Data Extraction: Extract Product With Custom Attributes From Browser HTML Only

Extracts product custom attributes from browser HTML only in Automatic Data Extraction.

```
GET https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-product-with-custom-attributes-from-browser-html-only
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automatic Data Extraction `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-product-with-custom-attributes-from-browser-html-only?connectionId=$CONNECTION_ID&customAttributes=%5Bobject%20Object%5D&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customAttributes": "[object Object]",
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/extract-product-with-custom-attributes-from-browser-html-only?${params}`, {
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
| `customAttributes` | object | yes |  |
| `url` | string | yes | Absolute URL to extract data from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customAttributes": {},
      "product": {},
      "statusCode": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customAttributes` | object |  |
| `product` | object |  |
| `statusCode` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Automatic Data Extraction API, this operation is `POST /extract` (base URL `https://api.zyte.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-product-with-custom-attributes-from-browser-html-only.md) for the provider-specific parameters and requirements.

