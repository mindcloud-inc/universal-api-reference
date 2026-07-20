# ApptiveGrid: List Space Invitations

Retrieves invitations from an ApptiveGrid space.

```
GET https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-space-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApptiveGrid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-space-invitations?connectionId=$CONNECTION_ID&spaceId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-space-invitations?${params}`, {
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
| `spaceId` | string | yes | The ApptiveGrid space id. |
| `userId` | string | yes | The ApptiveGrid user id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ApptiveGrid API returns.

## Native endpoint

Through the native ApptiveGrid API, this operation is `GET /api/users/:user_id/spaces/:space_id/invitations` (base URL `https://app.apptivegrid.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-invitations.md) for the provider-specific parameters and requirements.

