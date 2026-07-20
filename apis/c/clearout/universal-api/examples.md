# Clearout Universal API Examples

These examples use the MindCloud API key and Clearout connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Available Credits

Retrieves available credits from your Clearout account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-available-credits?${params}`, {
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
      "availableCredits": 1,
      "credits": {
        "available": 1,
        "availableDailyVerifyLimit": "string",
        "resetDailyVerifyLimitDate": "string",
        "subs": "string",
        "total": 1
      },
      "lowCreditBalanceMinThreshold": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Available Credits action reference](actions/get-available-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearout/latest/actions/get-available-credits).

## Cancel Bulk Email Finder Batch

Cancels a running bulk email finder batch in Clearout.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/cancel-bulk-email-finder-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clearout/latest/actions/cancel-bulk-email-finder-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string"
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
      "createdOn": "string",
      "name": "Ava Chen",
      "source": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Bulk Email Finder Batch action reference](actions/cancel-bulk-email-finder-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clearout/latest/actions/cancel-bulk-email-finder-batch).
