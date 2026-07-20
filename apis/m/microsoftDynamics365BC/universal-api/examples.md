# Microsoft Dynamics 365 BC Universal API Examples

These examples use the MindCloud API key and Microsoft Dynamics 365 BC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Credit Memo Itens ODataV4



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Credit Memo Itens ODataV4 action reference](actions/create-credit-memo-itens-o-data-v4.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4).

## Create Bank Deposit Lines ODataV4



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Bank Deposit Lines ODataV4 action reference](actions/create-bank-deposit-lines-o-data-v4.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365BC/latest/actions/create-bank-deposit-lines-o-data-v4).
