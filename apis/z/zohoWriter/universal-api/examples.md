# Zoho Writer Universal API Examples

These examples use the MindCloud API key and Zoho Writer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves documents from Zoho Writer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-documents?${params}`, {
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
      "documents": [
        {
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "type": "string"
        }
      ],
      "limit": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWriter/latest/actions/list-documents).

## Combine And Deliver Via Webhook

Combines documents and delivers them via webhook in Zoho Writer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-deliver-via-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/combine-and-deliver-via-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Combine And Deliver Via Webhook action reference](actions/combine-and-deliver-via-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoWriter/latest/actions/combine-and-deliver-via-webhook).
