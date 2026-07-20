# Zaia: List Responders

Retrieves responder identities from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-responders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-responders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-responders?${params}`, {
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
      "entity": "string",
      "id": "string",
      "name": "Ava Chen",
      "picture": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity` | string | Responder entity type. |
| `id` | string | Responder UUID. |
| `name` | string | Responder display name. |
| `picture` | string | Responder picture URL when available. |
| `workspaceId` | string | Workspace UUID associated with the responder. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/super-identities/responders` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-responders.md) for the provider-specific parameters and requirements.

