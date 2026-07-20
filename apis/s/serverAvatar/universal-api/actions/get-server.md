# ServerAvatar: Get Server

Retrieves a server from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server?${params}`, {
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
      "server": {
        "agentStatus": "string",
        "agentVersion": "string",
        "arch": "string",
        "cores": 1,
        "databaseType": "string",
        "filemanagerSlug": "string",
        "hostname": "Ava Chen",
        "id": 1,
        "ip": "string",
        "name": "Ava Chen",
        "operatingSystem": "string",
        "organizationId": 1,
        "phpCliVersion": "string",
        "phpmyadminSlug": "string",
        "phpVersions": [
          "string"
        ],
        "providerName": "Ava Chen",
        "redisPassword": "string",
        "sshPort": 1,
        "sshStatus": "string",
        "timezone": "string",
        "version": "string",
        "webServer": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `server` | object |  |
| `server.agentStatus` | string |  |
| `server.agentVersion` | string |  |
| `server.arch` | string |  |
| `server.cores` | number |  |
| `server.databaseType` | string |  |
| `server.filemanagerSlug` | string |  |
| `server.hostname` | string |  |
| `server.id` | number |  |
| `server.ip` | string |  |
| `server.name` | string |  |
| `server.operatingSystem` | string |  |
| `server.organizationId` | number |  |
| `server.phpCliVersion` | string |  |
| `server.phpmyadminSlug` | string |  |
| `server.phpVersions` | array<string> |  |
| `server.providerName` | string |  |
| `server.redisPassword` | string |  |
| `server.sshPort` | number |  |
| `server.sshStatus` | string |  |
| `server.timezone` | string |  |
| `server.version` | string |  |
| `server.webServer` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server.md) for the provider-specific parameters and requirements.

