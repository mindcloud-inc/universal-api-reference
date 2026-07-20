# SignRequest Universal API Examples

These examples use the MindCloud API key and SignRequest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List SignRequests



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/list-sign-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "disableAttachments": true,
      "disableBlockchainProof": true,
      "disableDate": true,
      "disableEmails": true,
      "disableText": true,
      "disableTextSignatures": true,
      "disableUploadSignatures": true,
      "document": "string",
      "forceSignatureColor": "string",
      "fromEmail": "ava@example.com",
      "fromEmailName": "ava@example.com",
      "integration": "string",
      "integrationData": {},
      "isBeingPrepared": true,
      "message": "string",
      "prepareUrl": "https://example.com",
      "redirectUrl": "https://example.com",
      "redirectUrlDeclined": "https://example.com",
      "requiredAttachments": [
        [
          {}
        ]
      ],
      "sendReminders": true,
      "signers": [
        [
          {}
        ]
      ],
      "subject": "string",
      "textMessageVerificationLocked": true,
      "url": "https://example.com",
      "uuid": "string",
      "who": "string"
    }
  ],
  "meta": {}
}
```

See the full [List SignRequests action reference](actions/list-sign-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signRequest/latest/actions/list-sign-requests).

## Cancel SignRequest



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/cancel-sign-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "38525278-876a-4f53-a69c-db39e82c753f"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/cancel-sign-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "38525278-876a-4f53-a69c-db39e82c753f"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cancelled": true,
      "detail": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel SignRequest action reference](actions/cancel-sign-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signRequest/latest/actions/cancel-sign-request).
