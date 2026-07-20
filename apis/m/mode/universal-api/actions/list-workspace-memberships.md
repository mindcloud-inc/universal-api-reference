# Mode: List Workspace Memberships

List members in a Mode workspace.

```
GET https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-workspace-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-workspace-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mode/latest/actions/list-workspace-memberships?${params}`, {
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
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "admin": true,
      "Links": {},
      "memberToken": "string",
      "memberUsername": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | date | Activation timestamp. |
| `admin` | boolean | Whether the member is an admin. |
| `Links` | object | Mode HAL links. |
| `memberToken` | string | Mode member token. |
| `memberUsername` | string | Mode username for the member. |
| `state` | string | Membership state. |

## Native endpoint

Through the native Mode API, this operation is `GET /memberships` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-memberships.md) for the provider-specific parameters and requirements.

