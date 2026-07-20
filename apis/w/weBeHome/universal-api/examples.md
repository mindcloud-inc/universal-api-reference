# WeBeHome Universal API Examples

These examples use the MindCloud API key and WeBeHome connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Customer Configuration



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration?connectionId=$CONNECTION_ID&HtmlTable=no&Heading=Yes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "HtmlTable": "no",
  "Heading": "Yes"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration?${params}`, {
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
      "BUID": 1,
      "CDT": "string",
      "CID": 1,
      "CN": "string",
      "CoID": 1,
      "CRDT": "string",
      "DDT": "string",
      "DESCR": "string",
      "LID": 1,
      "RIP": "string",
      "TZ": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Customer Configuration action reference](actions/get-customer-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weBeHome/latest/actions/get-customer-configuration).

## Accept User Terms Of Service



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/accept-user-terms-of-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/accept-user-terms-of-service', {
  method: 'PUT',
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
      "Created": "string"
    }
  ],
  "meta": {}
}
```

See the full [Accept User Terms Of Service action reference](actions/accept-user-terms-of-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weBeHome/latest/actions/accept-user-terms-of-service).
