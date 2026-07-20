# Byteplant Email Validator Universal API Examples

These examples use the MindCloud API key and Byteplant Email Validator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email Address

Retrieves email deliverability details from Byteplant Email Validator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&emailAddress=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address?${params}`, {
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
      "details": "string",
      "freemail": true,
      "info": "string",
      "ratelimitRemain": 1,
      "ratelimitSeconds": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Verify Email Address action reference](actions/verify-email-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/byteplantEmailValidator/latest/actions/verify-email-address).

## Create Bulk Email Validation Task

Creates a bulk email validation task in Byteplant Email Validator.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailsCsv": "Email\nsupport@byteplant.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailsCsv": "Email\nsupport@byteplant.com"
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
      "info": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Email Validation Task action reference](actions/create-bulk-email-validation-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/byteplantEmailValidator/latest/actions/create-bulk-email-validation-task).
