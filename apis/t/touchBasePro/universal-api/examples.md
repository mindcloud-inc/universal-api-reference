# TouchBasePro Universal API Examples

These examples use the MindCloud API key and TouchBasePro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Validation Credit Balance

Retrieves validation credit balance from TouchBasePro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-validation-credit-balance?${params}`, {
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
      "creditCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Validation Credit Balance action reference](actions/get-validation-credit-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/touchBasePro/latest/actions/get-validation-credit-balance).

## Activate Webhook

Activates an existing webhook in TouchBasePro.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/activate-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/activate-webhook', {
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
  "data": [],
  "meta": {}
}
```

See the full [Activate Webhook action reference](actions/activate-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/touchBasePro/latest/actions/activate-webhook).
