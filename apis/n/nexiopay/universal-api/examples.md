# Nexiopay Universal API Examples

These examples use the MindCloud API key and Nexiopay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Who am I



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/who-am-i?${params}`, {
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
      "accessRights": {},
      "accountId": "string",
      "accountType": "string",
      "businessLegalName": "Ava Chen",
      "cognitoSub": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateLastModified": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "firstName": "Ava",
      "isApiUser": true,
      "lastName": "Chen",
      "payoutAccessRights": {},
      "phone": "string",
      "userName": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Who am I action reference](actions/who-am-i.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nexiopay/latest/actions/who-am-i).

## Capture a transaction



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/capture-a-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/capture-a-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data": {}
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
      "amount": 1,
      "currency": "string",
      "id": "string",
      "merchantId": "string",
      "message": "string",
      "transactionStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Capture a transaction action reference](actions/capture-a-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nexiopay/latest/actions/capture-a-transaction).
