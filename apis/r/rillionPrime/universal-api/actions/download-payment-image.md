# Rillion Prime Pay: Download Payment Image



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/download-payment-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/download-payment-image?connectionId=$CONNECTION_ID&imageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/download-payment-image?${params}`, {
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
| `imageUrl` | string | yes | Use the full image URL returned by List Payment Images for check images. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "enableRangeProcessing": true,
      "entityTag": {},
      "fileContents": "string",
      "fileDownloadName": "Ava Chen",
      "lastModified": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `enableRangeProcessing` | boolean |  |
| `entityTag` | object |  |
| `fileContents` | string |  |
| `fileDownloadName` | string |  |
| `lastModified` | object |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/images/download` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-payment-image.md) for the provider-specific parameters and requirements.

