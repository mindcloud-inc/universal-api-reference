# Alto: Get Property Listing Images

Retrieves property image metadata from Alto.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-property-listing-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-property-listing-images?connectionId=$CONNECTION_ID&propertyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-property-listing-images?${params}`, {
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
| `propertyId` | string | yes | Unique Alto property identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalBrochures": [
        {}
      ],
      "floorplanImages": [
        {}
      ],
      "galleryImages": [
        {}
      ],
      "virtualTourImages": [
        {}
      ],
      "webLinks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalBrochures` | array<object> |  |
| `floorplanImages` | array<object> |  |
| `galleryImages` | array<object> |  |
| `virtualTourImages` | array<object> |  |
| `webLinks` | array<object> |  |

## Native endpoint

Through the native Alto API, this operation is `GET /listing/property/:propertyId/images` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-listing-images.md) for the provider-specific parameters and requirements.

