# Pabbly Hook: Delete Connections



```
DELETE https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-connections?connectionId=$CONNECTION_ID&connectionIds%5B%5D=conn_bdafbe30d2f04625822304af01e8216e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionIds[]": "conn_bdafbe30d2f04625822304af01e8216e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-connections?${params}`, {
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
| `connectionIds[]` | array<string> | yes | Connection IDs to move to trash. Example: `conn_bdafbe30d2f04625822304af01e8216e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "movedToTrash": 1,
      "permanentlyDeleted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Pabbly Hook connection deletion confirmation message. |
| `movedToTrash` | number | Number of connections moved to trash. |
| `permanentlyDeleted` | number | Number of connections permanently deleted. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `DELETE /api/v1/connections` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-connections.md) for the provider-specific parameters and requirements.

