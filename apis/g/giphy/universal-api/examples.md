# Giphy Universal API Examples

These examples use the MindCloud API key and Giphy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Random ID

Retrieves a random ID from Giphy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-random-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-random-id?${params}`, {
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
      "randomId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Random ID action reference](actions/get-random-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giphy/latest/actions/get-random-id).

## Register Content Action

Registers a GIF or sticker interaction in Giphy analytics.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/register-content-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "analyticsResponsePayload": "string",
  "actionType": "string",
  "randomId": "string",
  "ts": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giphy/latest/actions/register-content-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "analyticsResponsePayload": "string",
    "actionType": "string",
    "randomId": "string",
    "ts": 1
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
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [Register Content Action action reference](actions/register-content-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giphy/latest/actions/register-content-action).
