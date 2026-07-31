# Dev Excuses Universal API Examples

These examples use the MindCloud API key and Dev Excuses connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random Developer Excuse



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devExcuses/latest/actions/get-random-developer-excuse?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devExcuses/latest/actions/get-random-developer-excuse?${params}`, {
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
      "id": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random Developer Excuse action reference](actions/get-random-developer-excuse.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devExcuses/latest/actions/get-random-developer-excuse).
