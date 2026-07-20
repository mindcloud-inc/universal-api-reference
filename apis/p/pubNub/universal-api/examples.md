# PubNub Universal API Examples

These examples use the MindCloud API key and PubNub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage Metrics

Retrieves usage metrics from PubNub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-usage-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-usage-metrics?${params}`, {
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

See the full [Get Usage Metrics action reference](actions/get-usage-metrics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pubNub/latest/actions/get-usage-metrics).

## Assign Keysets To Customer

Assigns keysets to a PubNub customer.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/assign-keysets-to-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keysetIds[0]": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/assign-keysets-to-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keysetIds[0]": 1
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

See the full [Assign Keysets To Customer action reference](actions/assign-keysets-to-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pubNub/latest/actions/assign-keysets-to-customer).
