# SharpAPI: Generate Product Intro

Creates a product intro job in SharpAPI.

```
POST https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-intro
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-intro" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "Razer Blade 16 Gaming Laptop with RTX 4090, 32GB RAM, 2TB SSD, and dual-mode Mini LED display."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/generate-product-intro', {
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
| `content` | string | yes | Product name and its parameters to generate the product intro. Example: `Razer Blade 16 Gaming Laptop with RTX 4090, 32GB RAM, 2TB SSD, and dual-mode Mini LED display.`. |
| `language` | string | no | Specify the language of the output, defaults to English. Example: `English`. |
| `maxLength` | number | no | Specify the maximum length of the intro in number of words. Example: `200`. |
| `voiceTone` | string | no | Specify the voice tone of the output. It can be adjectives like funny or joyous, or even the name of a famous writer. Example: `neutral`. |

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

Through the native SharpAPI API, this operation is `POST /ecommerce/product_intro` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-product-intro.md) for the provider-specific parameters and requirements.

