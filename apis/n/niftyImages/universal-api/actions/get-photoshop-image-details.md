# NiftyImages: Get Photoshop Image Details

Retrieves Photoshop image details from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-photoshop-image-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-photoshop-image-details?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-photoshop-image-details?${params}`, {
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
| `url` | string | yes | NiftyImages image URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Hide": true,
      "LayerName": "Ava Chen",
      "LayerType": "string",
      "TextColor": "string",
      "TextValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Hide` | boolean |  |
| `LayerName` | string |  |
| `LayerType` | string |  |
| `TextColor` | string |  |
| `TextValue` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Psd` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photoshop-image-details.md) for the provider-specific parameters and requirements.

