# Baremetrics Universal API Examples

These examples use the MindCloud API key and Baremetrics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Baremetrics.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/get-account?${params}`, {
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

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baremetrics/latest/actions/get-account).

## Cancel Subscription

Cancels a subscription in Baremetrics.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/cancel-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionOid": "subscription_1",
  "sourceId": "source_1",
  "canceledAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baremetrics/latest/actions/cancel-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionOid": "subscription_1",
    "sourceId": "source_1",
    "canceledAt": "string"
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

See the full [Cancel Subscription action reference](actions/cancel-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/baremetrics/latest/actions/cancel-subscription).
