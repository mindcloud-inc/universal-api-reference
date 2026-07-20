# SharpAPI: Categorize Hospitality Product

Creates a hospitality product categorization job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-hospitality-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-hospitality-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Hotel Crystal Adults Only"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-hospitality-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Hotel Crystal Adults Only"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide the content to generate travel product categories. Example: `Hotel Crystal Adults Only`. |
| `city` | string | no | Specify the city to travel. Example: `Tokyo`. |
| `country` | string | no | Specify the country to travel. Example: `Japan`. |
| `language` | string | no | Specify the language of the output, defaults to English. Example: `English`. |
| `maxQuantity` | number | no | Maximum number of product categories to generate. Example: `10`. |
| `voiceTone` | string | no | Specify the voice tone. The default will be neutral. Example: `neutral`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | string | no | The list of other categories that will be taken into consideration during the mapping process. Example: `Luxury Hotels,Adults Only Hotels`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Provider job identifier for the submitted AI job. |
| `statusUrl` | string | Provider status URL for polling the AI job result. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /tth/hospitality_product_categories` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/categorize-hospitality-product.md) for the provider-specific parameters and requirements.

