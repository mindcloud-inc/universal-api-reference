# Checkmk Universal API Examples

These examples use the MindCloud API key and Checkmk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Activation Run

Retrieves activation run details from Checkmk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/get-activation-run?connectionId=$CONNECTION_ID&activationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/get-activation-run?${params}`, {
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
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Activation Run action reference](actions/get-activation-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkmk/latest/actions/get-activation-run).

## Acknowledge Host Problems

Creates host problem acknowledgements in Checkmk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/acknowledge-host-problems" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostName": "Ava Chen",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/acknowledge-host-problems', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostName": "Ava Chen",
    "comment": "string"
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
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Acknowledge Host Problems action reference](actions/acknowledge-host-problems.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/checkmk/latest/actions/acknowledge-host-problems).
