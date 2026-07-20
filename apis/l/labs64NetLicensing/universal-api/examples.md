# Labs64 NetLicensing Universal API Examples

These examples use the MindCloud API key and Labs64 NetLicensing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Licensees



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/list-licensees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/list-licensees?${params}`, {
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

See the full [List Licensees action reference](actions/list-licensees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/labs64NetLicensing/latest/actions/list-licensees).

## Create Bundle



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/create-bundle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/labs64NetLicensing/latest/actions/create-bundle', {
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

See the full [Create Bundle action reference](actions/create-bundle.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/labs64NetLicensing/latest/actions/create-bundle).
