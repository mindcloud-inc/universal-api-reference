# SparkPost Universal API Examples

These examples use the MindCloud API key and SparkPost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account?${params}`, {
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
      "anniversaryDate": "2026-05-07T12:00:00.000Z",
      "companyName": "Ava Chen",
      "countryCode": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "options": {},
      "serviceLevel": "string",
      "status": "string",
      "statusReasonCategory": "string",
      "statusUpdated": "2026-05-07T12:00:00.000Z",
      "subscription": {},
      "tfaRequired": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Account action reference](actions/retrieve-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sparkPost/latest/actions/retrieve-account).

## Create Recipient List



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-recipient-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "recipients[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/create-recipient-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "recipients[]": [{}]
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
      "id": "string",
      "name": "Ava Chen",
      "totalAcceptedRecipients": 1,
      "totalRejectedRecipients": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Recipient List action reference](actions/create-recipient-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sparkPost/latest/actions/create-recipient-list).
