# NiftyImages: Get Image Details

Retrieves image details from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-image-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-image-details?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-image-details?${params}`, {
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
      "CreateDate": "2026-05-07T12:00:00.000Z",
      "ImageType": "string",
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Opens": 1,
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreateDate` | date |  |
| `ImageType` | string |  |
| `LastUpdated` | date |  |
| `Name` | string |  |
| `Opens` | number |  |
| `Url` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Image` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-details.md) for the provider-specific parameters and requirements.

