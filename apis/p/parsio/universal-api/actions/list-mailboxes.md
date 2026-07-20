# Parsio: List Mailboxes



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-mailboxes?${params}`, {
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
      "collectEmails": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailPrefix": "ava@example.com",
      "isActive": true,
      "name": "Ava Chen",
      "processAttachments": true,
      "stats": {
        "docsFailed": 1,
        "docsParsed": 1,
        "docsTotal": 1
      },
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collectEmails` | boolean | Whether the mailbox collects email addresses. |
| `createdAt` | date | Mailbox creation timestamp. |
| `emailPrefix` | string | Mailbox email prefix. |
| `isActive` | boolean | Whether the mailbox is active. |
| `name` | string | Mailbox name. |
| `processAttachments` | boolean | Whether email attachments are processed. |
| `stats.docsFailed` | number | Total failed documents. |
| `stats.docsParsed` | number | Total parsed documents. |
| `stats.docsTotal` | number | Total documents received. |
| `status` | string | Mailbox status. |
| `updatedAt` | date | Mailbox update timestamp. |

## Native endpoint

Through the native Parsio API, this operation is `GET /mailboxes` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailboxes.md) for the provider-specific parameters and requirements.

