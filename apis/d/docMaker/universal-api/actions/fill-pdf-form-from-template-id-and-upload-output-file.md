# DocMaker: Fill PDF Form From Template ID And Upload Output File

Creates a filled PDF form from a template ID and uploads output in DocMaker.

```
POST https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-id-and-upload-output-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-id-and-upload-output-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateId": "s-w9-templ",
  "uploadOutputFile": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-id-and-upload-output-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateId": "s-w9-templ",
    "uploadOutputFile": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `templateId` | string | yes | Example: `s-w9-templ`. |
| `data` | object | no |  |
| `uploadOutputFile` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DocMaker API, this operation is `POST /fill_pdf` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-pdf-form-from-template-id-and-upload-output-file.md) for the provider-specific parameters and requirements.

