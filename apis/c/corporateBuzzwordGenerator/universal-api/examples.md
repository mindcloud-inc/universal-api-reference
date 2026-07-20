# Corporate Buzzword Generator Universal API Examples

These examples use the MindCloud API key and Corporate Buzzword Generator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Corporate Buzzword

Retrieves a random corporate buzzword phrase from Corporate Buzzword Generator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/corporateBuzzwordGenerator/latest/actions/generate-corporate-buzzword?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/corporateBuzzwordGenerator/latest/actions/generate-corporate-buzzword?${params}`, {
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
      "phrase": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Corporate Buzzword action reference](actions/generate-corporate-buzzword.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/corporateBuzzwordGenerator/latest/actions/generate-corporate-buzzword).
