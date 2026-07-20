# Mailform Universal API Examples

These examples use the MindCloud API key and Mailform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-current-user?${params}`, {
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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailform/latest/actions/get-current-user).

## Create Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": "USPS_FIRST_CLASS",
  "toName": "Frank White",
  "toAddress1": "607 North Avenue",
  "toCity": "Wakefield",
  "toState": "MA",
  "toPostcode": "01880",
  "toCountry": "US",
  "fromName": "Joe Green",
  "fromAddress1": "607 North Avenue",
  "fromCity": "Wakefield",
  "fromState": "MA",
  "fromPostcode": "01880",
  "fromCountry": "US"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailform/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": "USPS_FIRST_CLASS",
    "toName": "Frank White",
    "toAddress1": "607 North Avenue",
    "toCity": "Wakefield",
    "toState": "MA",
    "toPostcode": "01880",
    "toCountry": "US",
    "fromName": "Joe Green",
    "fromAddress1": "607 North Avenue",
    "fromCity": "Wakefield",
    "fromState": "MA",
    "fromPostcode": "01880",
    "fromCountry": "US"
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

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailform/latest/actions/create-order).
