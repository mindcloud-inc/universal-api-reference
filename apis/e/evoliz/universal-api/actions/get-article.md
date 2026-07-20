# Evoliz: Get Article

Retrieves an article from Evoliz.

```
GET https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evoliz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article?connectionId=$CONNECTION_ID&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evoliz/latest/actions/get-article?${params}`, {
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
| `articleId` | number | yes | The Evoliz article ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articleid": 1,
      "designation": "string",
      "enabled": true,
      "picture_link": "https://example.com",
      "quantity": 1,
      "reference": "string",
      "sale_classification": {
        "code": "string",
        "id": 1,
        "label": "string"
      },
      "stock_management": true,
      "stocked_quantity": 1,
      "ttc": true,
      "unit_price_vat_exclude": 1,
      "unit_price_vat_include": 1,
      "userid": 1,
      "vat": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articleid` | number |  |
| `designation` | string |  |
| `enabled` | boolean |  |
| `picture_link` | string |  |
| `quantity` | number |  |
| `reference` | string |  |
| `sale_classification.code` | string |  |
| `sale_classification.id` | number |  |
| `sale_classification.label` | string |  |
| `stock_management` | boolean |  |
| `stocked_quantity` | number |  |
| `ttc` | boolean |  |
| `unit_price_vat_exclude` | number |  |
| `unit_price_vat_include` | number |  |
| `userid` | number |  |
| `vat` | number |  |
| `weight` | number |  |

## Native endpoint

Through the native Evoliz API, this operation is `GET /api/v1/articles/:articleid` (base URL `https://www.evoliz.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

