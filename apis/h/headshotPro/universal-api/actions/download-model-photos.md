# HeadshotPro: Download Model Photos

Retrieves download URLs for model photos from HeadshotPro.

```
GET https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/download-model-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/download-model-photos?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/download-model-photos?${params}`, {
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
| `modelId` | string | yes | ID of the model whose photos should be downloaded. |
| `photoIds` | string | no | Optional subset of photo IDs to download. Leave empty to download all photos. Accepts multiple values as an array. |
| `include` | string | no | URL variants to include in the download response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloads": [
        {}
      ],
      "expiresAt": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloads` | array<object> | Download URL objects for the requested photos. |
| `expiresAt` | string | Timestamp when the signed download URLs expire. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `POST /organization/models/:modelId/photos/download` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-model-photos.md) for the provider-specific parameters and requirements.

