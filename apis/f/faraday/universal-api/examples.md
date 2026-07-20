# Faraday Universal API Examples

These examples use the MindCloud API key and Faraday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account Usage

Retrieves current account usage metrics from Faraday.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-current-account-usage?${params}`, {
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
      "finishedAt": "string",
      "id": "string",
      "startedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account Usage action reference](actions/get-current-account-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/faraday/latest/actions/get-current-account-usage).

## Archive Stream

Archives an existing stream in Faraday.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/archive-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/faraday/latest/actions/archive-stream', {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Archive Stream action reference](actions/archive-stream.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/faraday/latest/actions/archive-stream).
