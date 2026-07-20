# Encodian - Sign: Sign - Send File For Signature



```
POST https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/sign-send-file-for-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/sign-send-file-for-signature" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "sender": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/sign-send-file-for-signature', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "sender": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Set the name of the envelope. |
| `sender` | string | yes | Email address of the licensed sender for the workspace. |
| `file` | string | yes | Base64-encoded file content to submit for signature. |
| `message` | string | no | Message to share with recipients. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | no | Optional filename for the submitted file. |
| `labels[]` | array<string> | no | Labels to assign to the envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "envelopeId": "string",
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "labels": [
        "string"
      ],
      "message": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "operationId": "string",
      "operationStatus": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Date and time the envelope was created. |
| `envelopeId` | string | The unique identifier for the envelope. |
| `errors` | array<string> | Errors returned by Encodian. |
| `httpStatusCode` | number | HTTP status code for the response. |
| `httpStatusMessage` | string | HTTP status message for the response. |
| `labels` | array<string> | Labels assigned to the envelope. |
| `message` | string | Message shared with recipients. |
| `modified` | date | Date and time the envelope was modified. |
| `operationId` | string | Unique operation identifier. |
| `operationStatus` | string | Operation status. |
| `status` | string | Envelope status. |
| `title` | string | Envelope title. |

## Native endpoint

Through the native Encodian - Sign API, this operation is `POST /api/v1/Sign/EnvelopeCreateSingle` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-send-file-for-signature.md) for the provider-specific parameters and requirements.

