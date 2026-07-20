# Shopia Universal API Examples

These examples use the MindCloud API key and Shopia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Article Ideas



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "Productivity workflows",
  "audience": "SaaS founders"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopia/latest/actions/generate-article-ideas', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "Productivity workflows",
    "audience": "SaaS founders"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "outputs": [
        "string"
      ],
      "outputsPlainText": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Generate Article Ideas action reference](actions/generate-article-ideas.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopia/latest/actions/generate-article-ideas).
