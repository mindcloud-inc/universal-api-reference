# Omnara: Register Machine



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/register-machine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/register-machine" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/register-machine', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "machine": {
        "architecture": "string",
        "createdAt": "string",
        "daemonVersion": "string",
        "hostname": "Ava Chen",
        "id": "string",
        "lastSeenAt": "string",
        "metadata": {},
        "name": "Ava Chen",
        "platform": "string",
        "status": "string",
        "updatedAt": "string"
      },
      "machineToken": "string",
      "machineTokenExpiresIn": 1,
      "machineWsPath": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `machine` | object |  |
| `machine.architecture` | string |  |
| `machine.createdAt` | string |  |
| `machine.daemonVersion` | string |  |
| `machine.hostname` | string |  |
| `machine.id` | string |  |
| `machine.lastSeenAt` | string |  |
| `machine.metadata` | object |  |
| `machine.name` | string |  |
| `machine.platform` | string |  |
| `machine.status` | string |  |
| `machine.updatedAt` | string |  |
| `machineToken` | string |  |
| `machineTokenExpiresIn` | number |  |
| `machineWsPath` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/machines/register` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-machine.md) for the provider-specific parameters and requirements.

