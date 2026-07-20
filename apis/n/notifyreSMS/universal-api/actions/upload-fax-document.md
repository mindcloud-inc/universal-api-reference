# Notifyre SMS: Upload Fax Document

Uploads a fax document to Notifyre.

```
POST https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/upload-fax-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/upload-fax-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "base64Data": "string",
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/upload-fax-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "base64Data": "string",
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base64Data` | string | yes | Base64-encoded document contents. |
| `fileName` | string | yes | Original file name for conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string | Uploaded file name. |
| `id` | string | Conversion job identifier. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /fax/send/conversion` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-fax-document.md) for the provider-specific parameters and requirements.

