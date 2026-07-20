# PixelBin.io: Get Folder Details

Retrieves folder details from PixelBin.io storage.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-details?${params}`, {
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
| `name` | string | no | Folder name to fetch. |
| `path` | string | no | Path containing the folder. Use an empty string for the root path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "path": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | PixelBin folder identifier. |
| `isActive` | boolean | Whether the folder is active. |
| `name` | string | Folder name. |
| `path` | string | Parent folder path. |
| `type` | string | Returned resource type. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/folders` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-details.md) for the provider-specific parameters and requirements.

