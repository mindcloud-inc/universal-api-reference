# Lumin: Send Reminder Emails



```
PUT https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-reminder-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-reminder-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lumin/latest/actions/send-reminder-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | ID of the signature request. |
| `emails[]` | array<string> | yes | Array of signer email addresses to remind. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reminders": [
        {
          "email": "ava@example.com",
          "emailStatus": "ava@example.com",
          "signerStatus": "string"
        }
      ],
      "signatureRequest": {
        "createdAt": 1,
        "detailsUrl": "https://example.com",
        "expiresAt": 1,
        "signatureRequestId": "string",
        "signers": [
          {
            "email": "ava@example.com",
            "group": 1,
            "isApproved": true,
            "name": "Ava Chen",
            "status": "string"
          }
        ],
        "signingType": "string",
        "status": "string",
        "title": "string",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reminders[].email` | string |  |
| `reminders[].emailStatus` | string |  |
| `reminders[].signerStatus` | string |  |
| `signatureRequest.createdAt` | number |  |
| `signatureRequest.detailsUrl` | string |  |
| `signatureRequest.expiresAt` | number |  |
| `signatureRequest.signatureRequestId` | string |  |
| `signatureRequest.signers[].email` | string |  |
| `signatureRequest.signers[].group` | number |  |
| `signatureRequest.signers[].isApproved` | boolean |  |
| `signatureRequest.signers[].name` | string |  |
| `signatureRequest.signers[].status` | string |  |
| `signatureRequest.signingType` | string |  |
| `signatureRequest.status` | string |  |
| `signatureRequest.title` | string |  |
| `signatureRequest.updatedAt` | number |  |

## Native endpoint

Through the native Lumin API, this operation is `POST /signature_request/remind/:signature_request_id` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminder-emails.md) for the provider-specific parameters and requirements.

