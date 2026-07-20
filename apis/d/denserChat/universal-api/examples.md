# DenserChat Universal API Examples

These examples use the MindCloud API key and DenserChat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Chatbot

Retrieves a chatbot answer from DenserChat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot?connectionId=$CONNECTION_ID&question=What%20are%20the%20pricing%20options%20for%20denserbot%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "question": "What are the pricing options for denserbot?"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/denserChat/latest/actions/query-chatbot?${params}`, {
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
      "answer": "string",
      "passages": [
        {}
      ],
      "statusCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [Query Chatbot action reference](actions/query-chatbot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/denserChat/latest/actions/query-chatbot).
