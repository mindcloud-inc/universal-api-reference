# Open Letter Connect: Upload Template

Uploads a template to Open Letter Connect.

```
POST https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/upload-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/upload-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/upload-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `backHtml` | string | no | The optional back-side HTML file to upload. |
| `html` | string | no | The front HTML file to upload. |
| `thumbnail` | string | no | The thumbnail file to upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "backTemplatePath": "string",
        "templatePath": "string",
        "thumbnailPath": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.backTemplatePath` | string |  |
| `data.templatePath` | string |  |
| `data.thumbnailPath` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `POST /templates/upload` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-template.md) for the provider-specific parameters and requirements.

