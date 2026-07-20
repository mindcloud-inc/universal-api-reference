# Tidio Universal API Examples

These examples use the MindCloud API key and Tidio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact Messages [Plus plan]

Retrieves messages for a contact from Tidio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-messages-plus-plan?${params}`, {
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
      "conversationUrl": "https://example.com",
      "messages": [
        {
          "authorId": "string",
          "authorType": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "message": "string"
        }
      ],
      "meta": {
        "cursor": "string",
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Contact Messages [Plus plan] action reference](actions/get-contact-messages-plus-plan.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tidio/latest/actions/get-contact-messages-plus-plan).

## Add Website as Lyro Data Source [Plus plan]

Adds a website as a Lyro data source in Tidio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Website as Lyro Data Source [Plus plan] action reference](actions/add-website-as-lyro-data-source-plus-plan.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tidio/latest/actions/add-website-as-lyro-data-source-plus-plan).
