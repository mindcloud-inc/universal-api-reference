# Atlar Universal API Examples

These examples use the MindCloud API key and Atlar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List accounts

Retrieves accounts from Atlar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atlar/latest/actions/list-accounts?${params}`, {
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
      "items": [
        {}
      ],
      "limit": 1,
      "nextToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [List accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlar/latest/actions/list-accounts).

## Approve credit transfer

Approves a credit transfer in Atlar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/atlar/latest/actions/approve-credit-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "approvalStepId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atlar/latest/actions/approve-credit-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "approvalStepId": "string"
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
      "amount": {},
      "approvalSteps": [
        {}
      ],
      "attachedTransactions": [
        {}
      ],
      "categoryPurpose": "string",
      "chargeBearer": "string",
      "creatorUserId": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "destination": "string",
      "destinationHolder": {},
      "id": "string",
      "organizationId": "string",
      "reference": "string",
      "regulatoryReporting": [
        {}
      ],
      "scheme": "string",
      "schemeDetails": {},
      "source": {},
      "sourceHolder": {},
      "status": "string",
      "statusReason": {},
      "taxDetails": {}
    }
  ],
  "meta": {}
}
```

See the full [Approve credit transfer action reference](actions/approve-credit-transfer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/atlar/latest/actions/approve-credit-transfer).
