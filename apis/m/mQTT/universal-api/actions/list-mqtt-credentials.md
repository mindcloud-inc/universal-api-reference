# MQTT: List MQTT Credentials

Retrieves MQTT credentials from HiveMQ Cloud.

```
GET https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MQTT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mQTT/latest/actions/list-mqtt-credentials?${params}`, {
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
      "_links": {
        "next": "https://example.com"
      },
      "items": [
        {
          "roleRefs": [
            {
              "roleId": "string",
              "roleName": "Ava Chen"
            }
          ],
          "username": "Ava Chen"
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
| `_links.next` | string |  |
| `items[].roleRefs[].roleId` | string |  |
| `items[].roleRefs[].roleName` | string |  |
| `items[].username` | string |  |

## Native endpoint

Through the native MQTT API, this operation is `GET /mqtt/credentials` (base URL `https://api.a03.euc1.aws.hivemq.cloud/api/v2/orgs/q1zjbn/clusters/8a3176f6-5ba5-46f8-a7be-09c8032cefcd`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mqtt-credentials.md) for the provider-specific parameters and requirements.

