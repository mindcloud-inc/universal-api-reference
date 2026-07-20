# TeleSign Universal API Examples

These examples use the MindCloud API key and TeleSign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Phone Number Channel Capability



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability?connectionId=$CONNECTION_ID&channel=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability?${params}`, {
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
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Check Phone Number Channel Capability action reference](actions/check-phone-number-channel-capability.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teleSign/latest/actions/check-phone-number-channel-capability).

## Create Masked SMS Session



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/create-masked-sms-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/create-masked-sms-session', {
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
  "data": [
    {
      "external_id": "string",
      "reference_id": "string",
      "session_data": {
        "phone_number_1": {
          "masked_id": "string"
        },
        "phone_number_2": {
          "masked_id": "string"
        },
        "resource": "string",
        "session_end_on": "string",
        "validity": "string"
      },
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Masked SMS Session action reference](actions/create-masked-sms-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teleSign/latest/actions/create-masked-sms-session).
