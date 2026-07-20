# Column Universal API Examples

These examples use the MindCloud API key and Column connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Financial Institutions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-financial-institutions?${params}`, {
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
      "achEligible": true,
      "checkEligible": true,
      "city": "string",
      "countryCode": "string",
      "createdAt": "string",
      "fullName": "Ava Chen",
      "phoneNumber": "string",
      "realtimeEligible": true,
      "realtimeRfpEligible": true,
      "routingNumber": "string",
      "routingNumberType": "string",
      "shortName": "Ava Chen",
      "state": "string",
      "streetAddress": "string",
      "updatedAt": "string",
      "wireEligible": true,
      "wireSettlementOnly": true,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Financial Institutions action reference](actions/list-financial-institutions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/column/latest/actions/list-financial-institutions).

## Cancel ACH Transfer



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/column/latest/actions/cancel-ach-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "achTransferId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/cancel-ach-transfer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "achTransferId": "string"
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

See the full [Cancel ACH Transfer action reference](actions/cancel-ach-transfer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/column/latest/actions/cancel-ach-transfer).
