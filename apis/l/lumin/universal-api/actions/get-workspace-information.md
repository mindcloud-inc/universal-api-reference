# Lumin: Get Workspace Information



```
GET https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-workspace-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-workspace-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lumin/latest/actions/get-workspace-information?${params}`, {
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
      "workspace": {
        "createdAt": 1,
        "id": "string",
        "name": "Ava Chen",
        "owner": "string",
        "totalMembers": 1,
        "totalSpaces": 1,
        "userRole": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspace.createdAt` | number |  |
| `workspace.id` | string |  |
| `workspace.name` | string |  |
| `workspace.owner` | string |  |
| `workspace.totalMembers` | number |  |
| `workspace.totalSpaces` | number |  |
| `workspace.userRole` | string |  |

## Native endpoint

Through the native Lumin API, this operation is `GET /workspaces/info` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-information.md) for the provider-specific parameters and requirements.

