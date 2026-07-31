# Placecats Universal API Examples

These examples use the MindCloud API key and Placecats connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Grayscale Cat Placeholder



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-grayscale-cat-placeholder?connectionId=$CONNECTION_ID&width=1&height=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "width": "1",
  "height": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placecats/latest/actions/get-grayscale-cat-placeholder?${params}`, {
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Grayscale Cat Placeholder action reference](actions/get-grayscale-cat-placeholder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placecats/latest/actions/get-grayscale-cat-placeholder).
