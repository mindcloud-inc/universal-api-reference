# Cutt.ly Universal API Examples

These examples use the MindCloud API key and Cutt.ly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Link Statistics

Retrieves click statistics for a shortened link in Cutt.ly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics?connectionId=$CONNECTION_ID&stats=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stats": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics?${params}`, {
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
      "bots": "string",
      "clicks": 1,
      "date": "string",
      "devices": {},
      "facebook": 1,
      "fullLink": "https://example.com",
      "googlePlus": 1,
      "instagram": 1,
      "linkedin": 1,
      "pinterest": 1,
      "refs": {},
      "rest": 1,
      "shortLink": "https://example.com",
      "status": 1,
      "title": "string",
      "twitter": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Link Statistics action reference](actions/get-link-statistics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cuttly/latest/actions/get-link-statistics).

## Add Link Tag

Adds a tag to a shortened link in Cutt.ly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/add-link-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "edit": "string",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/add-link-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "edit": "string",
    "tag": "string"
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
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Link Tag action reference](actions/add-link-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cuttly/latest/actions/add-link-tag).
