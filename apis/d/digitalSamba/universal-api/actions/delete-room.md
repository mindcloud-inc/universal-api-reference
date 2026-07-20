# Digital Samba: Delete room

Deletes an existing room from Digital Samba.

```
DELETE https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/delete-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/delete-room?connectionId=$CONNECTION_ID&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/delete-room?${params}`, {
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
| `room` | string | yes | Room path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON request body documented for this endpoint. |
| `deleteResources` | boolean | no | If `true`, permanently deletes all session content for this room. Defaults to `false`. |
| `deleteHistory` | boolean | no | If `true`, anonymises PII for all archived participants of this room. Defaults to `false`. |
| `deleteLibrary` | boolean | no | If `true`, deletes the room's content library. Defaults to `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digital Samba API returns.

## Native endpoint

Through the native Digital Samba API, this operation is `DELETE /rooms/:room` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room.md) for the provider-specific parameters and requirements.

