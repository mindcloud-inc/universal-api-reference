# Contentful Universal API Examples

These examples use the MindCloud API key and Contentful connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List spaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/list-spaces?${params}`, {
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
        {
          "name": "Ava Chen",
          "sys": {
            "id": "string",
            "type": "string"
          }
        }
      ],
      "limit": 1,
      "skip": 1,
      "sys": {
        "type": "string"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List spaces action reference](actions/list-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentful/latest/actions/list-spaces).

## Activate content type



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/activate-content-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentful/latest/actions/activate-content-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "displayField": "string",
      "fields": [
        {
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "sys": {
        "firstPublishedAt": "2026-05-07T12:00:00.000Z",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "publishedCounter": 1,
        "publishedVersion": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Activate content type action reference](actions/activate-content-type.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentful/latest/actions/activate-content-type).
