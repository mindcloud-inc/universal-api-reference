# NiftyImages: List Bee Plugin User Images

Retrieves Bee Plugin user images from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-user-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-user-images?connectionId=$CONNECTION_ID&pluginKey=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pluginKey": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/list-bee-plugin-user-images?${params}`, {
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
| `pluginKey` | string | yes | Bee Plugin key. |
| `user` | string | yes | User identifier. |
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
      "Name": "Ava Chen",
      "Opens": 1,
      "Status": "string",
      "Uri": "string",
      "UserName": "Ava Chen"
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
| `Name` | string |  |
| `Opens` | number |  |
| `Status` | string |  |
| `Uri` | string |  |
| `UserName` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /BeePlugin/:pluginKey/Users/:user` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bee-plugin-user-images.md) for the provider-specific parameters and requirements.

