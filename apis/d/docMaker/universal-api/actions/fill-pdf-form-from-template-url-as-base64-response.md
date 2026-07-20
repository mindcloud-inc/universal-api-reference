# DocMaker: Fill PDF Form From Template URL As Base64 Response

Creates a filled PDF form from a template URL as Base64 in DocMaker.

```
POST https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-url-as-base64-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocMaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-url-as-base64-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docMaker/latest/actions/fill-pdf-form-from-template-url-as-base64-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `templateUrl` | string | yes |  |
| `data` | object | no |  |
| `metadata` | string | no |  |

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
| `jobId` | string | DocMaker job identifier for the PDF form request |
| `status` | string | DocMaker job creation status |

## Native endpoint

Through the native DocMaker API, this operation is `POST /fill_pdf` (base URL `https://api.v2.docmaker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-pdf-form-from-template-url-as-base64-response.md) for the provider-specific parameters and requirements.

