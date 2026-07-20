# G2 Universal API Examples

These examples use the MindCloud API key and G2 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Categories

Retrieves categories from G2.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories?${params}`, {
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
      "attributes": {
        "description": "string",
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "string",
        "uuid": "string"
      },
      "id": "string",
      "relationships": {
        "ancestors": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "parent": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "products": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Categories action reference](actions/list-categories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/g2/latest/actions/list-categories).
