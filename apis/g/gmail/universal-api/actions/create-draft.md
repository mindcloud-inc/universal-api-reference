# Google Mail: Create Draft

Creates a Gmail draft.

```
POST https://connect.mindcloud.co/v1/universal/gmail/latest/actions/create-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/create-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/create-draft', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | no | Recipient email address. Use a comma-separated list for multiple recipients. Example: `alice@example.com, bob@example.com`. |
| `subject` | string | no | Draft subject line. Example: `Quick follow-up`. |
| `bodyText` | string | no | Plain-text draft body. If both Body Text and Body HTML are provided, Body Text is rendered above Body HTML. Example: `Hello,\n\nDrafting this for review...\n`. |
| `bodyHtml` | string | no | HTML draft body. If both Body Text and Body HTML are provided, Body Text is rendered above Body HTML. Example: `<p>Hello from MindCloud</p>`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cc` | string | no | Optional CC recipients. Use a comma-separated list. Example: `manager@example.com`. |
| `bcc` | string | no | Optional BCC recipients. Use a comma-separated list. Example: `audit@example.com`. |
| `from` | string | no | Optional sender header. Must be permitted by Gmail account configuration. Example: `me@example.com`. |
| `replyTo` | string | no | Optional Reply-To address. Example: `replyto@example.com`. |
| `threadId` | string | no | Optional Gmail thread ID when adding the draft to an existing thread. Example: `19c7cd447accadc2`. |
| `inReplyTo` | string | no | Optional RFC 2822 In-Reply-To header for threaded replies. Example: `<message-id@example.com>`. |
| `references` | string | no | Optional RFC 2822 References header for threaded replies. Example: `<first@example.com> <second@example.com>`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": {
        "id": "string",
        "labelIds": [
          "string"
        ],
        "threadId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message.id` | string |  |
| `message.labelIds[]` | string |  |
| `message.threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /drafts` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft.md) for the provider-specific parameters and requirements.

