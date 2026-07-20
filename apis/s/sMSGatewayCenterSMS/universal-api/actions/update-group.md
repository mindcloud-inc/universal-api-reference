# SMSGatewayCenter SMS: Update Group



```
PUT https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGatewayCenter SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "groupName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSGatewayCenterSMS/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "groupName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the SMSGatewayCenter group to update. |
| `groupName` | string | yes | New name for the SMSGatewayCenter contact group. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.action` | string | Provider action name. |
| `response.api` | string | Provider API family. |
| `response.code` | string | Provider response code. |
| `response.msg` | string | Provider message. |
| `response.status` | string | Provider status label. |

## Native endpoint

Through the native SMSGatewayCenter SMS API, this operation is `POST /SMSApi/group/update` (base URL `https://unify.smsgateway.center`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

