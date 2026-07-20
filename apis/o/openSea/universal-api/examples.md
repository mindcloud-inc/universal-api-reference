# OpenSea Universal API Examples

These examples use the MindCloud API key and OpenSea connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Supported Chains Catalog

Retrieves supported chains from OpenSea.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains?${params}`, {
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
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Supported Chains Catalog action reference](actions/get-chains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openSea/latest/actions/get-chains).

## Create Criteria Offer

Creates a criteria offer in OpenSea.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-criteria-offer-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "protocolData": {},
  "criteria": {},
  "protocolAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-criteria-offer-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "protocolData": {},
    "criteria": {},
    "protocolAddress": "string"
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
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Criteria Offer action reference](actions/post-criteria-offer-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openSea/latest/actions/post-criteria-offer-v2).
