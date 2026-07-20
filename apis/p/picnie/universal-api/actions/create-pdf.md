# Picnie: Create PDF

Creates a PDF in Picnie from a template.

```
POST https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "templateId": "2075",
  "templateName": "Simple Happy Thanksgiving",
  "details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/create-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "templateId": "2075",
    "templateName": "Simple Happy Thanksgiving",
    "details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project ID that will own the generated PDF. |
| `templateId` | number | yes | Template ID to use for PDF generation. Example: `2075`. |
| `templateName` | string | yes | Template name expected by Picnie. Example: `Simple Happy Thanksgiving`. |
| `details` | object<object> | yes | Template field values to merge into the generated PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /create-pdf` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pdf.md) for the provider-specific parameters and requirements.

