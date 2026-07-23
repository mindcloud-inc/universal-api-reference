# Microsoft Exchange Universal API Examples

These examples use the MindCloud API key and Microsoft Exchange connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authorize Application



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/authorize-application?${params}`, {
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
      "accessToken": "string",
      "expiresIn": 1,
      "extExpiresIn": 1,
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authorize Application action reference](actions/authorize-application.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftExchange/latest/actions/authorize-application).

## Add File Attachment to Message

Creates a file attachment on a message in Microsoft Exchange.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/add-file-attachment-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "name": "Ava Chen",
  "contentType": "text/plain",
  "contentBytes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/add-file-attachment-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "name": "Ava Chen",
    "contentType": "text/plain",
    "contentBytes": "string"
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
      "@odata": {
        "type": "string"
      },
      "contentBytes": "string",
      "contentType": "string",
      "id": "string",
      "isInline": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

See the full [Add File Attachment to Message action reference](actions/add-file-attachment-to-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftExchange/latest/actions/add-file-attachment-to-message).
