# Track-POD Universal API Examples

These examples use the MindCloud API key and Track-POD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authorization

Retrieves authorization and rate limit status from Track-POD.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/test-authorization?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Authorization action reference](actions/test-authorization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackPOD/latest/actions/test-authorization).

## Add Driver

Creates a new driver in Track-POD.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-driver', {
  method: 'POST',
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
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Driver action reference](actions/add-driver.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackPOD/latest/actions/add-driver).
