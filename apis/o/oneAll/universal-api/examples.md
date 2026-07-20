# OneAll Universal API Examples

These examples use the MindCloud API key and OneAll connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves all site users from OneAll.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/list-users?${params}`, {
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
      "response": {
        "request": {
          "date": "2026-05-07T12:00:00.000Z",
          "resource": "string",
          "status": {
            "code": 1,
            "flag": "string",
            "info": "string"
          }
        },
        "result": {
          "data": {
            "users": {
              "count": 1,
              "pagination": {
                "currentPage": 1,
                "entriesPerPage": 1,
                "order": {
                  "direction": "string",
                  "field": "string"
                },
                "totalEntries": 1,
                "totalPages": 1
              }
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneAll/latest/actions/list-users).

## Cast Vote

Casts a LoudVoice vote in OneAll.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/cast-vote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorToken": "string",
  "commentToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneAll/latest/actions/cast-vote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorToken": "string",
    "commentToken": "string"
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

See the full [Cast Vote action reference](actions/cast-vote.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneAll/latest/actions/cast-vote).
