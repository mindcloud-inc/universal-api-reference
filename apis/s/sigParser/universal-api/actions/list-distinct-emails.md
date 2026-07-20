# SigParser: List Distinct Emails



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/list-distinct-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/list-distinct-emails?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/list-distinct-emails?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "cc": [
        {}
      ],
      "conversationIndex": 1,
      "date": "string",
      "from": {},
      "id": "string",
      "ingestionKey": 1,
      "inReplyTo": "string",
      "internetMessageid": "string",
      "mailboxinstance": {},
      "references": [
        "string"
      ],
      "subject": "string",
      "to": [
        {}
      ],
      "type": "string",
      "virtualConversationid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Email attachments. |
| `cc` | array<object> | Recipients in the CC field. |
| `conversationIndex` | number | Zero-based position in the conversation. |
| `date` | string | Email date and time. |
| `from` | object | Sender details. |
| `id` | string | SigParser email record ID. |
| `ingestionKey` | number | Ingestion watermark for incremental syncs. |
| `inReplyTo` | string | Reply-to message ID. |
| `internetMessageid` | string | MIME Message-ID value when present. |
| `mailboxinstance` | object | Mailbox instance metadata. |
| `references` | array<string> | Referenced message IDs in the thread. |
| `subject` | string | Email subject line. |
| `to` | array<object> | Recipients in the To field. |
| `type` | string | Email type such as inbound, outbound, or internal. |
| `virtualConversationid` | string | Derived conversation ID. |

## Native endpoint

Through the native SigParser API, this operation is `GET /api/Emails/Distinct` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-distinct-emails.md) for the provider-specific parameters and requirements.

