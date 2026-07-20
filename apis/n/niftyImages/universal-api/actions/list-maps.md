# NiftyImages: List Maps

Retrieves maps from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-maps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-maps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-maps?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "CreateDate": "2026-05-07T12:00:00.000Z",
      "ImageType": "string",
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Opens": "string",
      "Url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `CreateDate` | date |  |
| `ImageType` | string |  |
| `LastUpdated` | date |  |
| `Name` | string |  |
| `Opens` | string |  |
| `Url` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Maps` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-maps.md) for the provider-specific parameters and requirements.

