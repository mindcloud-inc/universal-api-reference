# Socket: List GitHub Repositories

Retrieves GitHub repositories available in Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-git-hub-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-git-hub-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-git-hub-repositories?${params}`, {
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
      "results": [
        {
          "createdAt": "string",
          "githubFullName": "Ava Chen",
          "githubInstallId": "string",
          "githubRepoId": "string",
          "id": "string",
          "latestProjectReport": {
            "createdAt": "string",
            "id": "string"
          },
          "name": "Ava Chen",
          "organizationId": "string",
          "updatedAt": "string",
          "workspace": "string"
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
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].createdAt` | string |  |
| `results[].githubFullName` | string |  |
| `results[].githubInstallId` | string |  |
| `results[].githubRepoId` | string |  |
| `results[].id` | string |  |
| `results[].latestProjectReport` | object |  |
| `results[].latestProjectReport.createdAt` | string |  |
| `results[].latestProjectReport.id` | string |  |
| `results[].name` | string |  |
| `results[].organizationId` | string |  |
| `results[].updatedAt` | string |  |
| `results[].workspace` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /repo/list` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-git-hub-repositories.md) for the provider-specific parameters and requirements.

