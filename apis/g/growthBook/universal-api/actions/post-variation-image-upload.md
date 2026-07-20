# GrowthBook: Upload a variation screenshot

Uploads a variation screenshot to GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-variation-image-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-variation-image-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "prj_19g6smo332up7",
  "variationId": "0",
  "screenshot": "sample",
  "contentType": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-variation-image-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "prj_19g6smo332up7",
    "variationId": "0",
    "screenshot": "sample",
    "contentType": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `prj_19g6smo332up7`. |
| `variationId` | string | yes | Default: `0`. |
| `screenshot` | string | yes | Base64-encoded screenshot data Default: `sample`. |
| `contentType` | string | yes | MIME type of the screenshot Default: `sample`. |
| `description` | string | no | Optional description for the screenshot |

## Response

```json
{
  "success": true,
  "data": [
    {
      "screenshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `screenshot` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /experiments/:id/variation/:variationId/screenshot/upload` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-variation-image-upload.md) for the provider-specific parameters and requirements.

