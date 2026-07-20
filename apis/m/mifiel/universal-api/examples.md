# Mifiel Universal API Examples

These examples use the MindCloud API key and Mifiel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Webhooks

Retrieves webhook endpoint records from Mifiel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/list-webhooks?${params}`, {
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
      "callback_type": "string",
      "created_at": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Webhooks action reference](actions/list-webhooks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mifiel/latest/actions/list-webhooks).

## Create Document

Creates a new document in Mifiel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "signatories[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mifiel/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "signatories[].email": "ava@example.com"
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "original_hash": "string",
      "signed": true,
      "signers": [
        {}
      ],
      "state": "string",
      "viewers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mifiel/latest/actions/create-document).
