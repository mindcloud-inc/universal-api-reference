# MQTT: Create MQTT Credential

Creates a new MQTT credential in HiveMQ Cloud.

```
POST https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-credential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentials.password": "string",
  "credentials.username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/create-mqtt-credential', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentials.password": "string",
    "credentials.username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `credentials.password` | string | yes | Password for the new MQTT credential |
| `credentials.username` | string | yes | Username for the new MQTT credential |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userInfo": {
        "roleRefs": [
          {
            "roleId": "string",
            "roleName": "Ava Chen"
          }
        ],
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `userInfo.roleRefs[].roleId` | string |  |
| `userInfo.roleRefs[].roleName` | string |  |
| `userInfo.username` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `POST /mqtt/credentials` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mqtt-credential.md) for the provider-specific parameters and requirements.

