# LogRocket Universal API Examples

These examples use the MindCloud API key and LogRocket connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Highlights Result



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result?connectionId=$CONNECTION_ID&id=highlights%20request%20id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "highlights request id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/get-highlights-result?${params}`, {
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
      "appID": "string",
      "requestID": "string",
      "result": {
        "highlights": "string",
        "sessions": [
          {
            "highlights": "string",
            "recordingID": "string",
            "sessionID": 1
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Highlights Result action reference](actions/get-highlights-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logRocket/latest/actions/get-highlights-result).

## Request User Highlights



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/request-user-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logRocket/latest/actions/request-user-highlights', {
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Request User Highlights action reference](actions/request-user-highlights.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logRocket/latest/actions/request-user-highlights).
