# MillionVerifier Universal API Examples

These examples use the MindCloud API key and MillionVerifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Credits

Retrieves available API credits from MillionVerifier.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/get-api-credits?${params}`, {
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
      "bulkCredits": 1,
      "credits": 1,
      "plan": 1,
      "renewingCredits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get API Credits action reference](actions/get-api-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/millionVerifier/latest/actions/get-api-credits).

## Stop Verification File

Stops a verification file in MillionVerifier.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/stop-verification-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/millionVerifier/latest/actions/stop-verification-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": 1
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Stop Verification File action reference](actions/stop-verification-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/millionVerifier/latest/actions/stop-verification-file).
