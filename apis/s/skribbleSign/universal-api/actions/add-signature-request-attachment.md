# Skribble Sign: Add Signature Request Attachment

Adds an attachment to a signature request in Skribble Sign.

```
POST https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-attachment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "filename": "Ava Chen",
  "contentType": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-attachment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "filename": "Ava Chen",
    "contentType": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The signature request ID. |
| `filename` | string | yes | The attachment filename. |
| `contentType` | string | yes | The attachment MIME type. |
| `content` | string | yes | The base64 encoded attachment content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_type": "string",
      "filename": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_type` | string | Attachment MIME type. |
| `filename` | string | Attachment filename. |
| `id` | string | Attachment ID. |

## Native endpoint

Through the native Skribble Sign API, this operation is `POST /v2/signature-requests/:signatureRequestId/attachments` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-signature-request-attachment.md) for the provider-specific parameters and requirements.

