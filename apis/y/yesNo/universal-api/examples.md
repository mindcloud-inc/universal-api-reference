# Yes/No Universal API Examples

These examples use the MindCloud API key and Yes/No connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Answer



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yesNo/latest/actions/get-answer?${params}`, {
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
      "forced": true,
      "image": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Answer action reference](actions/get-answer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yesNo/latest/actions/get-answer).
