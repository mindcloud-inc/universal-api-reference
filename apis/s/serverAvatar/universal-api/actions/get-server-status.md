# ServerAvatar: Get Server Status

Retrieves server status from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-status?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-status?${params}`, {
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
      "configurationInPercentage": 1,
      "key": "string",
      "label": "string",
      "record": [
        {
          "key": "string",
          "label": "string",
          "percentage": 1,
          "status": "string"
        }
      ],
      "server": {
        "arch": "string",
        "cloudProviderId": "string",
        "cores": 1,
        "hostname": "Ava Chen",
        "id": 1,
        "ip": "string",
        "name": "Ava Chen",
        "operatingSystem": "string",
        "organizationId": 1,
        "providerName": "Ava Chen",
        "serverInstanceId": 1,
        "version": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configurationInPercentage` | number |  |
| `key` | string |  |
| `label` | string |  |
| `record` | array<object> |  |
| `record[].key` | string |  |
| `record[].label` | string |  |
| `record[].percentage` | number |  |
| `record[].status` | string |  |
| `server` | object |  |
| `server.arch` | string |  |
| `server.cloudProviderId` | string |  |
| `server.cores` | number |  |
| `server.hostname` | string |  |
| `server.id` | number |  |
| `server.ip` | string |  |
| `server.name` | string |  |
| `server.operatingSystem` | string |  |
| `server.organizationId` | number |  |
| `server.providerName` | string |  |
| `server.serverInstanceId` | number |  |
| `server.version` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/status` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-status.md) for the provider-specific parameters and requirements.

