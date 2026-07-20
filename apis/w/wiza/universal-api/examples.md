# Wiza Universal API Examples

These examples use the MindCloud API key and Wiza connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your remaining Wiza credits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits?${params}`, {
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
      "credits": {
        "apiCredits": 1,
        "emailCredits": "ava@example.com",
        "exportCredits": 1,
        "phoneCredits": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiza/latest/actions/get-credits).

## Continue Prospect Search

Continues a previous prospect search in Wiza.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/continue-prospect-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiza/latest/actions/continue-prospect-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "data": {
        "enrichment_level": "string",
        "finished_at": "string",
        "id": 1,
        "name": "Ava Chen",
        "stats": {
          "people": 1
        },
        "status": "string"
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Continue Prospect Search action reference](actions/continue-prospect-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiza/latest/actions/continue-prospect-search).
