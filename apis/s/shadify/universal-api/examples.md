# Shadify Universal API Examples

These examples use the MindCloud API key and Shadify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Addition Expression

Retrieves a random addition expression from Shadify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-addition-expression?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-addition-expression?${params}`, {
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
      "answer": 1,
      "expression": "string",
      "first": 1,
      "operation": "string",
      "second": 1
    }
  ],
  "meta": {}
}
```

See the full [Generate Addition Expression action reference](actions/generate-addition-expression.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shadify/latest/actions/generate-addition-expression).
