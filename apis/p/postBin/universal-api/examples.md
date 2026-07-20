# PostBin Universal API Examples

These examples use the MindCloud API key and PostBin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bin

Retrieves a PostBin bin by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin?connectionId=$CONNECTION_ID&binId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "binId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postBin/latest/actions/get-bin?${params}`, {
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
      "binId": "string",
      "expires": 1,
      "now": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Bin action reference](actions/get-bin.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postBin/latest/actions/get-bin).

## Create Bin

Creates a new PostBin bin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postBin/latest/actions/create-bin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postBin/latest/actions/create-bin', {
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
      "binId": "string",
      "expires": 1,
      "now": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bin action reference](actions/create-bin.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postBin/latest/actions/create-bin).
