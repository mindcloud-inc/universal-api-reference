# EMnify Universal API Examples

These examples use the MindCloud API key and EMnify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Endpoint Details

Retrieves details for an endpoint from EMnify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token&endpointId=18811970" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token",
  "endpointId": "18811970"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-details?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "imei": {},
      "imeiLock": true,
      "imeiWithLuhn": {},
      "ipAddress": "string",
      "ipAddressSpace": {
        "id": 1,
        "ipAddressSpace": "string",
        "ipAddressVersion": 1
      },
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "serviceProfile": {
        "id": 1,
        "name": "Ava Chen"
      },
      "status": {
        "description": "string",
        "id": 1
      },
      "tags": {},
      "tariffProfile": {
        "id": 1,
        "name": "Ava Chen",
        "satelliteCapable": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Endpoint Details action reference](actions/get-endpoint-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eMnify/latest/actions/get-endpoint-details).

## Create Application Token

Creates a new application token in EMnify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-application-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/create-application-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authToken": "Paste the auth_token from Retrieve Authentication Token"
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
      "applicationToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Application Token action reference](actions/create-application-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eMnify/latest/actions/create-application-token).
