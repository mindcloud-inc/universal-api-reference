# MQTT: Get MQTT Credential

Retrieves an MQTT credential from HiveMQ Cloud by username.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-credential
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-credential?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/get-mqtt-credential?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | MQTT credential username |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credentials": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credentials[].userInfo.roleRefs[].roleId` | string |  |
| `credentials[].userInfo.roleRefs[].roleName` | string |  |
| `credentials[].userInfo.username` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/credentials/username/:username` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mqtt-credential.md) for the provider-specific parameters and requirements.

