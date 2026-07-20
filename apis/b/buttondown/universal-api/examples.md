# Buttondown Universal API Examples

These examples use the MindCloud API key and Buttondown connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Newsletters

Retrieves newsletters from Buttondown.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-newsletters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-newsletters?${params}`, {
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
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Newsletters action reference](actions/list-newsletters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buttondown/latest/actions/list-newsletters).

## Create Draft Email

Creates a draft email in Buttondown.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/create-draft-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/create-draft-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "body": "string"
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
      "absoluteUrl": "https://example.com",
      "analytics": {},
      "attachments": [
        {}
      ],
      "body": "string",
      "canonicalUrl": "https://example.com",
      "commentingMode": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "emailType": "ava@example.com",
      "featured": true,
      "filters": {},
      "id": "string",
      "image": "string",
      "metadata": {},
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "publishDate": "2026-05-07T12:00:00.000Z",
      "relatedEmailIds": [
        "ava@example.com"
      ],
      "reviewMode": "string",
      "secondaryId": 1,
      "shouldTriggerPayPerEmailBilling": true,
      "slug": "string",
      "source": "string",
      "status": "string",
      "subject": "string",
      "suppressionReason": "string",
      "template": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Draft Email action reference](actions/create-draft-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buttondown/latest/actions/create-draft-email).
