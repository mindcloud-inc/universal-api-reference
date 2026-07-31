# Techy Universal API Examples

These examples use the MindCloud API key and Techy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Techy Phrase



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/techy/latest/actions/get-random-techy-phrase?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Techy Phrase action reference](actions/get-random-techy-phrase.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/techy/latest/actions/get-random-techy-phrase).
