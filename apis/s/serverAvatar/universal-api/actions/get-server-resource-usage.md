# ServerAvatar: Get Server Resource Usage

Retrieves server resource usage from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-resource-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-resource-usage?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-resource-usage?${params}`, {
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
| `organization` | string | yes |  |
| `server` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cores": 1,
      "disk": {
        "total": 1,
        "usage": 1,
        "usageInPercentage": 1
      },
      "memory": {
        "available": 1,
        "total": 1
      },
      "serverInfo": {
        "nodeVersion": "string",
        "npmVersion": "string",
        "processor": "string",
        "restartRequired": "string",
        "timezone": "string"
      },
      "serverLoad": 1,
      "serverUptime": "string",
      "swapMemory": {
        "available": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cores` | number |  |
| `disk` | object |  |
| `disk.total` | number |  |
| `disk.usage` | number |  |
| `disk.usageInPercentage` | number |  |
| `memory` | object |  |
| `memory.available` | number |  |
| `memory.total` | number |  |
| `serverInfo` | object |  |
| `serverInfo.nodeVersion` | string |  |
| `serverInfo.npmVersion` | string |  |
| `serverInfo.processor` | string |  |
| `serverInfo.restartRequired` | string |  |
| `serverInfo.timezone` | string |  |
| `serverLoad` | number |  |
| `serverUptime` | string |  |
| `swapMemory` | object |  |
| `swapMemory.available` | number |  |
| `swapMemory.total` | number |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/usage` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-resource-usage.md) for the provider-specific parameters and requirements.

