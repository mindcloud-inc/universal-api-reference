# Postbode Universal API Examples

These examples use the MindCloud API key and Postbode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mailboxes

Retrieves available mailboxes from the Postbode API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postbode/latest/actions/list-mailboxes?${params}`, {
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
      "available_balance": 1,
      "balance": 1,
      "id": 1,
      "name": "Ava Chen",
      "vat_shifted": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Mailboxes action reference](actions/list-mailboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postbode/latest/actions/list-mailboxes).

## Create Letter Draft

Creates a draft letter in a Postbode mailbox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postbode/latest/actions/create-letter-draft" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/postbode/latest/actions/create-letter-draft', {
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

Example response:

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

See the full [Create Letter Draft action reference](actions/create-letter-draft.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postbode/latest/actions/create-letter-draft).
