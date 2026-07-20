# SMSGatewayCenter SMS Universal API Examples

These examples use the MindCloud API key and SMSGatewayCenter SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/read-profile?${params}`, {
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
      "response": {
        "account": {},
        "action": "string",
        "api": "string",
        "code": "string",
        "count": 1,
        "msg": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Read Profile action reference](actions/read-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSGatewayCenterSMS/latest/actions/read-profile).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactName": "Ava Chen",
  "mobileNo": "string",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactName": "Ava Chen",
    "mobileNo": "string",
    "groupId": "string"
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
      "response": {
        "action": "string",
        "api": "string",
        "code": "string",
        "msg": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSGatewayCenterSMS/latest/actions/create-contact).
