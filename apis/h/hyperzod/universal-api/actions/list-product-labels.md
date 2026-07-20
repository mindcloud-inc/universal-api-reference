# Hyperzod: List Product Labels

Retrieves a list of product labels from Hyperzod.

```
GET https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-product-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperzod `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-product-labels?connectionId=$CONNECTION_ID&merchantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "merchantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-product-labels?${params}`, {
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
| `merchantId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the Hyperzod request completed successfully. |

## Native endpoint

Through the native Hyperzod API, this operation is `GET /merchant/v1/catalog/product-label/list` (base URL `https://api.hyperzod.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-labels.md) for the provider-specific parameters and requirements.

