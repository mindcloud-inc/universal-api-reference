# Botsonic Universal API Examples

These examples use the MindCloud API key and Botsonic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List FAQs

Retrieves all FAQs from a Botsonic bot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-faqs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/list-faqs?${params}`, {
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
      "items": [
        {}
      ],
      "page": 1,
      "pages": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List FAQs action reference](actions/list-faqs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botsonic/latest/actions/list-faqs).

## Bulk Upload URLs

Uploads multiple URLs as bot data in Botsonic.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/bulk-upload-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": "https://example.com/help/article"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botsonic/latest/actions/bulk-upload-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": "https://example.com/help/article"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Bulk Upload URLs action reference](actions/bulk-upload-urls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botsonic/latest/actions/bulk-upload-urls).
