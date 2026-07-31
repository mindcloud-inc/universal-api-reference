# GoT Quotes Universal API Examples

These examples use the MindCloud API key and GoT Quotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Character



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character?${params}`, {
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
      "": [
        {
          "house": {
            "name": "Ava Chen",
            "slug": "string"
          },
          "name": "Ava Chen",
          "quotes": [
            "string"
          ],
          "slug": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Character action reference](actions/get-character.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goTQuotes/latest/actions/get-character).
