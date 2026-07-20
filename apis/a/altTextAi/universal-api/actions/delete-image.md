# AltText.Ai: Delete Image

Deletes an image from your AltText.Ai library.

```
DELETE https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/delete-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/delete-image?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/delete-image?${params}`, {
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
| `assetId` | string | yes | The asset ID of the image to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "altTexts": {},
      "assetId": "string",
      "createdAt": 1,
      "errorCode": "string",
      "errors": {},
      "metadata": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `altTexts` | object |  |
| `assetId` | string |  |
| `createdAt` | number |  |
| `errorCode` | string |  |
| `errors` | object |  |
| `metadata` | object |  |
| `tags` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native AltText.Ai API, this operation is `DELETE /images/:asset_id` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image.md) for the provider-specific parameters and requirements.

