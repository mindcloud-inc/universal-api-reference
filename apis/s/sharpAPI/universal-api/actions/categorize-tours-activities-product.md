# SharpAPI: Categorize Tours Activities Product

Creates a tours activities categorization job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-tours-activities-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-tours-activities-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Oasis of the Bay"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/categorize-tours-activities-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Oasis of the Bay"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide the content to generate travel product categories. Example: `Oasis of the Bay`. |
| `city` | string | no | Specify the city of travel. Example: `Ha Long`. |
| `country` | string | no | Specify the country related to travel. Example: `Vietnam`. |
| `language` | string | no | Specify the language of the output, defaults to English. Example: `English`. |
| `maxQuantity` | number | no | Specify the maximum number of product categories to generate. Example: `10`. |
| `voiceTone` | string | no | Specify the voice tone of the output. Example: `neutral`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `context` | string | no | The list of other categories that will be taken into consideration during the mapping process. Example: `Boat Tours,Halong Bay Cruises`. |

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
| `jobId` | string | SharpAPI job identifier for the submitted job. |
| `statusUrl` | string | SharpAPI status URL for the submitted job. |

## Native endpoint

Through the native SharpAPI API, this operation is `POST /tth/ta_product_categories` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/categorize-tours-activities-product.md) for the provider-specific parameters and requirements.

