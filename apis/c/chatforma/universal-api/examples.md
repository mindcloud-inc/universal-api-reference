# Chatforma Universal API Examples

These examples use the MindCloud API key and Chatforma connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves current account authorization status from Chatforma.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-current-account?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatforma/latest/actions/get-current-account).

## Add User To Segment

Adds a user to a Chatforma segment.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/add-user-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "segmentId": 1,
  "botUserId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/add-user-to-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "segmentId": 1,
    "botUserId": 1
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

See the full [Add User To Segment action reference](actions/add-user-to-segment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatforma/latest/actions/add-user-to-segment).
