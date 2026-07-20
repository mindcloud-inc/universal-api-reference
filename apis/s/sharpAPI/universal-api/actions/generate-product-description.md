# SharpAPI: Generate Product Description

Creates a product description job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Razer Blade 16 Gaming Laptop with RTX 4090, 32GB RAM, 2TB SSD, and dual-mode Mini LED display."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-description', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "Razer Blade 16 Gaming Laptop with RTX 4090, 32GB RAM, 2TB SSD, and dual-mode Mini LED display."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Provide product information to generate a product description. Example: `Razer Blade 16 Gaming Laptop with RTX 4090, 32GB RAM, 2TB SSD, and dual-mode Mini LED display.`. |

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

Through the native SharpAPI API, this operation is `POST /ecommerce/product_description` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-product-description.md) for the provider-specific parameters and requirements.

