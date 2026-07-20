# Printful: Get Product Size Guide

Retrieves a size guide for a Printful catalog product.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-product-size-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-product-size-guide?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-product-size-guide?${params}`, {
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
| `id` | string | yes | The Printful product id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fit": "string",
      "measurements": {},
      "size": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fit` | string |  |
| `measurements` | object |  |
| `size` | string |  |

## Native endpoint

Through the native Printful API, this operation is `GET /products/{id}/sizes` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-size-guide.md) for the provider-specific parameters and requirements.

