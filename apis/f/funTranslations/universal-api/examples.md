# Fun Translations Universal API Examples

These examples use the MindCloud API key and Fun Translations connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Translate to Dothraki



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-dothraki?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/funTranslations/latest/actions/translate-dothraki?${params}`, {
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
      "contents": {},
      "success": {}
    }
  ],
  "meta": {}
}
```

See the full [Translate to Dothraki action reference](actions/translate-dothraki.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/funTranslations/latest/actions/translate-dothraki).
