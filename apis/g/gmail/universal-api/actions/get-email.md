# Google Mail: Get Email

Retrieves a Gmail message.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-email?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The immutable ID of the message.. Use the List Emails action to find this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "historyId": "string",
      "labelIds": [
        "string"
      ],
      "messageLink": "https://example.com",
      "originalHeaders": {
        "arcAuthenticationResults": "string",
        "arcMessageSignature": "string",
        "arcSeal": "string",
        "authenticationResults": "string",
        "autoSubmitted": "string",
        "contentType": "string",
        "date": "string",
        "deliveredTo": "string",
        "dkimSignature": "string",
        "feedbackId": "string",
        "from": "string",
        "inReplyTo": "string",
        "messageId": "string",
        "mimeVersion": "string",
        "received": "string",
        "receivedSpf": "string",
        "references": "string",
        "replyTo": "string",
        "returnPath": "string",
        "subject": "string",
        "to": "string",
        "xGoogleSmtpSource": "string",
        "xReceived": "string",
        "xSesOutgoing": "string",
        "xSlackMessageId": "string",
        "xSlackTeamId": "string"
      },
      "simpleHeaders": {
        "recipient": "string",
        "sender": "string",
        "subject": "string",
        "threadTopic": "string"
      },
      "snippet": "string",
      "subject": "string",
      "textContent": "string",
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string |  |
| `historyId` | string |  |
| `labelIds[]` | string |  |
| `messageLink` | string |  |
| `originalHeaders.arcAuthenticationResults` | string |  |
| `originalHeaders.arcMessageSignature` | string |  |
| `originalHeaders.arcSeal` | string |  |
| `originalHeaders.authenticationResults` | string |  |
| `originalHeaders.autoSubmitted` | string |  |
| `originalHeaders.contentType` | string |  |
| `originalHeaders.date` | string |  |
| `originalHeaders.deliveredTo` | string |  |
| `originalHeaders.dkimSignature` | string |  |
| `originalHeaders.feedbackId` | string |  |
| `originalHeaders.from` | string |  |
| `originalHeaders.inReplyTo` | string |  |
| `originalHeaders.messageId` | string |  |
| `originalHeaders.mimeVersion` | string |  |
| `originalHeaders.received` | string |  |
| `originalHeaders.receivedSpf` | string |  |
| `originalHeaders.references` | string |  |
| `originalHeaders.replyTo` | string |  |
| `originalHeaders.returnPath` | string |  |
| `originalHeaders.subject` | string |  |
| `originalHeaders.to` | string |  |
| `originalHeaders.xGoogleSmtpSource` | string |  |
| `originalHeaders.xReceived` | string |  |
| `originalHeaders.xSesOutgoing` | string |  |
| `originalHeaders.xSlackMessageId` | string |  |
| `originalHeaders.xSlackTeamId` | string |  |
| `simpleHeaders.recipient` | string |  |
| `simpleHeaders.sender` | string |  |
| `simpleHeaders.subject` | string |  |
| `simpleHeaders.threadTopic` | string |  |
| `snippet` | string |  |
| `subject` | string |  |
| `textContent` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /messages/:id` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

