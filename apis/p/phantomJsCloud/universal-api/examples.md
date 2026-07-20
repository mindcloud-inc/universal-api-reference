# PhantomJsCloud Universal API Examples

These examples use the MindCloud API key and PhantomJsCloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Render Page as Text

Renders a page as plain text in PhantomJsCloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/render-page-as-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/render-page-as-text?${params}`, {
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

See the full [Render Page as Text action reference](actions/render-page-as-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phantomJsCloud/latest/actions/render-page-as-text).
