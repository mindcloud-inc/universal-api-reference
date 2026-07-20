# WebCategorize Universal API Examples

These examples use the MindCloud API key and WebCategorize connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List URL Tags



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List URL Tags action reference](actions/list-url-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webCategorize/latest/actions/list-url-tags).

## Add Content Feedback



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/add-content-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentId": "string",
  "score": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/add-content-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentId": "string",
    "score": 1
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Content Feedback action reference](actions/add-content-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webCategorize/latest/actions/add-content-feedback).
