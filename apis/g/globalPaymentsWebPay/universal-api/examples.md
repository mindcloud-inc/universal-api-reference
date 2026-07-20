# Global Payments WebPay Universal API Examples

These examples use the MindCloud API key and Global Payments WebPay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts

Retrieves accounts from Global Payments WebPay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/list-accounts?${params}`, {
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
      "accounts": [
        {
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "type": "string"
        }
      ],
      "current_page_size": 1,
      "paging": {
        "page": 1,
        "page_size": 1
      },
      "total_record_count": 1
    }
  ],
  "meta": {}
}
```

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalPaymentsWebPay/latest/actions/list-accounts).

## Accept Dispute

Updates a dispute by accepting it in Global Payments WebPay.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/accept-dispute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/accept-dispute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "action": {
        "id": "string"
      },
      "amount": "string",
      "currency": "string",
      "id": "string",
      "reason_code": "string",
      "result": "string",
      "stage": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept Dispute action reference](actions/accept-dispute.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalPaymentsWebPay/latest/actions/accept-dispute).
