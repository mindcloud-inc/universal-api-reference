# MQTT: List Role Permissions

Retrieves MQTT role permissions from HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-role-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-role-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-role-permissions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "rolePermissions": [
        {
          "permissionId": "string",
          "roleId": "string",
          "roleName": "Ava Chen"
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
| `rolePermissions[].permissionId` | string |  |
| `rolePermissions[].roleId` | string |  |
| `rolePermissions[].roleName` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/roles/permissions` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-role-permissions.md) for the provider-specific parameters and requirements.

