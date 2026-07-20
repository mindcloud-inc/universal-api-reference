# NiftyImages: List Widget Images

Retrieves widget images from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widget-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widget-images?connectionId=$CONNECTION_ID&widgetKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-widget-images?${params}`, {
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
| `widgetKey` | string | yes | Widget key. |
| `startDate` | string | no | Start date in ISO 8601 format. |
| `endDate` | string | no | End date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ImageID": 1,
      "ImageType": "string",
      "Impressions": 1,
      "Name": "Ava Chen",
      "Suspended": true,
      "Uri": "string",
      "User": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ImageID` | number |  |
| `ImageType` | string |  |
| `Impressions` | number |  |
| `Name` | string |  |
| `Suspended` | boolean |  |
| `Uri` | string |  |
| `User` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Widgets/:widgetKey/Images` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-widget-images.md) for the provider-specific parameters and requirements.

