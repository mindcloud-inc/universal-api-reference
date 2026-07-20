# ShipWise Universal API Examples

These examples use the MindCloud API key and ShipWise connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Token V2

Validates an API token in ShipWise.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/validate-token-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/validate-token-v2?${params}`, {
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

See the full [Validate Token V2 action reference](actions/validate-token-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipWise/latest/actions/validate-token-v2).

## Add Carrier Service V2

Creates a carrier service in ShipWise.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/add-carrier-service-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/add-carrier-service-v2', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Carrier Service V2 action reference](actions/add-carrier-service-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipWise/latest/actions/add-carrier-service-v2).
