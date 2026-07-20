# AltTextify: Delete Image

Deletes an image from AltTextify by asset ID.

```
DELETE https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/delete-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltTextify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/delete-image?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/delete-image?${params}`, {
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
| `assetId` | string | yes | The AltTextify asset ID of the image to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt_text": [
        "string"
      ],
      "asset_id": "string",
      "created_date": "2026-05-07T12:00:00.000Z",
      "image_source": "string",
      "status": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt_text` | array<string> |  |
| `asset_id` | string |  |
| `created_date` | date |  |
| `image_source` | string |  |
| `status` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native AltTextify API, this operation is `DELETE /image/:asset_id` (base URL `https://api.alttextify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image.md) for the provider-specific parameters and requirements.

