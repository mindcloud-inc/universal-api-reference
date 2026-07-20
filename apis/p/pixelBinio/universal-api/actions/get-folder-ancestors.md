# PixelBin.io: Get Folder Ancestors

Retrieves folder ancestors from PixelBin.io storage.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-ancestors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-ancestors?connectionId=$CONNECTION_ID&_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-folder-ancestors?${params}`, {
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
| `_id` | string | yes | PixelBin folder _id returned by List Files or Get Folder Details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ancestors": [
        {}
      ],
      "folder": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ancestors` | array<object> | Ancestor folders ordered from root to parent. |
| `folder` | object | Resolved folder record. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/assets/v1.0/folders/:_id/ancestors` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder-ancestors.md) for the provider-specific parameters and requirements.

