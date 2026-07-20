# Next Cloud OCS Universal API Examples

These examples use the MindCloud API key and Next Cloud OCS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Capabilities

Retrieves capabilities from Next Cloud OCS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/get-capabilities?${params}`, {
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
      "data": {},
      "message": "string",
      "ocs": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Capabilities action reference](actions/get-capabilities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextCloudOCS/latest/actions/get-capabilities).

## Accept Cloud Share

Accepts a cloud share in Next Cloud OCS.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/accept-cloud-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextCloudOCS/latest/actions/accept-cloud-share', {
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
      "data": {},
      "message": "string",
      "ocs": {},
      "status": "string",
      "statuscode": 1
    }
  ],
  "meta": {}
}
```

See the full [Accept Cloud Share action reference](actions/accept-cloud-share.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextCloudOCS/latest/actions/accept-cloud-share).
