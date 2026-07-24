# Rillion Prime Pay: List Payment Images



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-images?connectionId=$CONNECTION_ID&paymentId=string&imageType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "string",
  "imageType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-images?${params}`, {
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
| `paymentId` | string | yes | Payment ID to fetch images for. |
| `imageType` | list<string> | yes | Image type to return for the payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageExtension": "string",
      "images": [
        {
          "imageName": "Ava Chen",
          "imageUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageExtension` | string |  |
| `images[].imageName` | string |  |
| `images[].imageUrl` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/images` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-images.md) for the provider-specific parameters and requirements.

