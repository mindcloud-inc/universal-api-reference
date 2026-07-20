# iLovePDF: Create Signature Request

Creates a signature request in iLovePDF.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/create-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/create-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/create-signature-request', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "about_to_expire_reminder": true,
      "certified": true,
      "completed_on": "string",
      "created": "string",
      "email": "ava@example.com",
      "expired": true,
      "expires": "string",
      "expiring": true,
      "files": [
        {
          "filename": "Ava Chen",
          "filesize": 1,
          "pages": 1
        }
      ],
      "language": "string",
      "lock_order": true,
      "message_signer": "string",
      "mode": "string",
      "name": "Ava Chen",
      "notes": "string",
      "signer_reminder_days_cycle": 1,
      "signer_reminders": true,
      "signers": [
        {
          "access_code": true,
          "email": "ava@example.com",
          "force_signature_type": "string",
          "name": "Ava Chen",
          "notes": "string",
          "phone": "string",
          "phone_access_code": true,
          "status": "string",
          "token_requester": "string",
          "type": "string",
          "uuid": "string"
        }
      ],
      "status": "string",
      "subject_cc": "string",
      "subject_signer": "string",
      "timezone": "string",
      "token_requester": "string",
      "uuid": "string",
      "uuid_visible": true,
      "verify_enabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about_to_expire_reminder` | boolean |  |
| `certified` | boolean |  |
| `completed_on` | string |  |
| `created` | string |  |
| `email` | string |  |
| `expired` | boolean |  |
| `expires` | string |  |
| `expiring` | boolean |  |
| `files[].filename` | string |  |
| `files[].filesize` | number |  |
| `files[].pages` | number |  |
| `language` | string |  |
| `lock_order` | boolean |  |
| `message_signer` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `signer_reminder_days_cycle` | number |  |
| `signer_reminders` | boolean |  |
| `signers[].access_code` | boolean |  |
| `signers[].email` | string |  |
| `signers[].force_signature_type` | string |  |
| `signers[].name` | string |  |
| `signers[].notes` | string |  |
| `signers[].phone` | string |  |
| `signers[].phone_access_code` | boolean |  |
| `signers[].status` | string |  |
| `signers[].token_requester` | string |  |
| `signers[].type` | string |  |
| `signers[].uuid` | string |  |
| `status` | string |  |
| `subject_cc` | string |  |
| `subject_signer` | string |  |
| `timezone` | string |  |
| `token_requester` | string |  |
| `uuid` | string |  |
| `uuid_visible` | boolean |  |
| `verify_enabled` | boolean |  |

## Native endpoint

Through the native iLovePDF API, this operation is `POST https://:server/v1/signature` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signature-request.md) for the provider-specific parameters and requirements.

