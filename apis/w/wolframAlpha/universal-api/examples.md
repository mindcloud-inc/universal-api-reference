# Wolfram Alpha Universal API Examples

These examples use the MindCloud API key and Wolfram Alpha connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Short Answer

Retrieves a short text answer from Wolfram Alpha.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-short-answer?connectionId=$CONNECTION_ID&i=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "i": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-short-answer?${params}`, {
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
      "query": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Short Answer action reference](actions/get-short-answer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wolframAlpha/latest/actions/get-short-answer).
