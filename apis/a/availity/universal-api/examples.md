# Availity Universal API Examples

These examples use the MindCloud API key and Availity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payers

Retrieves payers and supported transactions from Availity.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/availity/latest/actions/list-payers?${params}`, {
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
      "displayName": "Ava Chen",
      "name": "Ava Chen",
      "payerId": "string",
      "processingRoutes": {}
    }
  ],
  "meta": {}
}
```

See the full [List Payers action reference](actions/list-payers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/availity/latest/actions/list-payers).

## Create Claim Status Inquiry

Creates a claim status inquiry in Availity.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-claim-status-inquiry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/availity/latest/actions/create-claim-status-inquiry', {
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
      "claimAmount": "string",
      "claimCount": "string",
      "controlNumber": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "fromDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {},
      "patient": {},
      "payer": {},
      "providers": [
        {}
      ],
      "status": "string",
      "statusCode": "string",
      "submitter": {},
      "subscriber": {},
      "toDate": "2026-05-07T12:00:00.000Z",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Claim Status Inquiry action reference](actions/create-claim-status-inquiry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/availity/latest/actions/create-claim-status-inquiry).
