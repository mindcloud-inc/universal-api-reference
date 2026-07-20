# DocuPipe Universal API Examples

These examples use the MindCloud API key and DocuPipe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information

Retrieves account information from DocuPipe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information?${params}`, {
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
      "awsContractDetails": {},
      "billingMethod": "string",
      "overageCredits": 1,
      "overageEnabled": true,
      "planCosts": {},
      "planName": "Ava Chen",
      "remainingCredits": 1,
      "renewalDate": "2026-05-07T12:00:00.000Z",
      "retentionDays": 1,
      "upcomingInvoice": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuPipe/latest/actions/get-account-information).

## Add a Class

Creates a class in DocuPipe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/add-a-class" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "className": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/add-a-class', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "className": "Ava Chen"
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
      "classId": "string",
      "className": "Ava Chen",
      "description": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add a Class action reference](actions/add-a-class.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuPipe/latest/actions/add-a-class).
