# Tisane Labs Universal API Examples

These examples use the MindCloud API key and Tisane Labs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Languages

Retrieves supported languages from Tisane Labs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/list-languages?${params}`, {
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
      "encoding": "string",
      "englishName": "Ava Chen",
      "fontFace": "string",
      "isLatinScript": true,
      "isoCode": "string",
      "loaded": true,
      "name": "Ava Chen",
      "rightToLeft": true,
      "segmentation": "string",
      "systemLanguage": true
    }
  ],
  "meta": {}
}
```

See the full [List Languages action reference](actions/list-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tisaneLabs/latest/actions/list-languages).
