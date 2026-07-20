# Florm: Get My Workspace

Retrieves your private workspace from Florm.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-my-workspace?${params}`, {
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
      "guid": "string",
      "name": "Ava Chen",
      "slug": "string",
      "teamGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guid` | string | GUID of the current Florm workspace. |
| `name` | string | Workspace name. |
| `slug` | string | Workspace slug. |
| `teamGuid` | string | GUID of the owning team. |

## Native endpoint

Through the native Florm API, this operation is `GET /v1/workspaces/my` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-workspace.md) for the provider-specific parameters and requirements.

