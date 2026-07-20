# Particle Universal API Examples

These examples use the MindCloud API key and Particle connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user?${params}`, {
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
      "accountInfo": {
        "accountType": "string",
        "businessAccount": true,
        "businessCategory": "string",
        "companyName": "Ava Chen",
        "firstName": "Ava",
        "lastName": "Chen"
      },
      "cellularDeviceCount": 1,
      "memberships": [
        {}
      ],
      "mfa": {
        "enabled": true
      },
      "tos": {
        "accepted": true,
        "date": "string",
        "version": 1
      },
      "username": "Ava Chen",
      "wifiDeviceCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/particle/latest/actions/get-current-user).

## Call Device Function



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/particle/latest/actions/call-device-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "arg": "test",
  "deviceId": "0123456789abcdef01234567",
  "functionName": "testFunction"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/particle/latest/actions/call-device-function', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "arg": "test",
    "deviceId": "0123456789abcdef01234567",
    "functionName": "testFunction"
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
      "connected": true,
      "id": "string",
      "returnValue": 1
    }
  ],
  "meta": {}
}
```

See the full [Call Device Function action reference](actions/call-device-function.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/particle/latest/actions/call-device-function).
