# Nautical Universal API Examples

These examples use the MindCloud API key and Nautical connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Retrieves a list of orders from Nautical.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders?${params}`, {
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
      "data": {
        "orders": {
          "edges": [
            {
              "node": {
                "created": "string",
                "id": "string",
                "number": "string",
                "status": "string"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nautical/latest/actions/list-orders).
