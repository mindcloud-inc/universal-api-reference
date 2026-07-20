# Postbode: Send Letter

Creates and sends a letter from a Postbode mailbox.

```
POST https://connect.mindcloud.co/v1/universal/postbode/latest/actions/send-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postbode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/send-letter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailboxId": "155198",
  "documents[]": [
    {}
  ],
  "documents[].name": "letter.pdf",
  "documents[].content": "Base64-encoded PDF"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postbode/latest/actions/send-letter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailboxId": "155198",
    "documents[]": [{}],
    "documents[].name": "letter.pdf",
    "documents[].content": "Base64-encoded PDF"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailboxId` | number | yes | The Postbode mailbox ID. Example: `155198`. |
| `documents[]` | array<object> | yes | One or more PDF documents to upload. |
| `documents[].name` | string | yes | The filename that Postbode should store for the PDF. Example: `letter.pdf`. |
| `documents[].content` | string | yes | The PDF file encoded as base64. Example: `Base64-encoded PDF`. |
| `envelopeId` | number | no | Envelope option ID for the outgoing letter. Example: `2`. |
| `country` | string | no | Destination country code, for example NL. Example: `NL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "letter_id": 1,
      "reference": "string",
      "response_code": 1,
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `letter_id` | number |  |
| `reference` | string |  |
| `response_code` | number |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Postbode API, this operation is `POST /mailbox/:mailbox_id/letters` (base URL `https://app.postbode.nu/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-letter.md) for the provider-specific parameters and requirements.

