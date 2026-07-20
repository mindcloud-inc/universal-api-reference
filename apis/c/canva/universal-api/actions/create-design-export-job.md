# Canva: Create Design Export Job

Creates a design export job in Canva.

```
POST https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design-export-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design-export-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "DAVZr1z5464",
  "format": {},
  "format.type": "gif"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/create-design-export-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "DAVZr1z5464",
    "format": {},
    "format.type": "gif"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designId` | string | yes | The design ID. Example: `DAVZr1z5464`. |
| `format` | object | yes | Details about the desired export format. |
| `format.type` | list<string> | yes | The export file format type. One of: `gif`, `jpg`, `mp4`, `pdf`, `png`, `pptx`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format.exportQuality` | list<string> | no | Specifies the export quality of the design. One of: `pro`, `regular`. |
| `format.quality` | string | no | The media quality setting for JPG or MP4 exports. |
| `format.size` | list<string> | no | The paper size of the export PDF file. One of: `a3`, `a4`, `legal`, `letter`. |
| `format.height` | number | no | The export height in pixels. Example: `400`. |
| `format.width` | number | no | The export width in pixels. Example: `400`. |
| `format.pages[]` | array<number> | no | Page numbers to export from a multi-page design. Example: `2,3,4`. |
| `format.lossless` | boolean | no | Whether to export the PNG without compression. |
| `format.transparentBackground` | boolean | no | Whether to export the PNG with a transparent background. |
| `format.asSingleImage` | boolean | no | Whether to merge a multi-page PNG export into a single image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "error": {
          "code": "string",
          "message": "string"
        },
        "id": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.error.code` | string | Provider error code when the export job fails. |
| `job.error.message` | string | Provider error message when the export job fails. |
| `job.id` | string | Canva export job ID. |
| `job.status` | string | Current export job status. |

## Native endpoint

Through the native Canva API, this operation is `POST /v1/exports` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-design-export-job.md) for the provider-specific parameters and requirements.

