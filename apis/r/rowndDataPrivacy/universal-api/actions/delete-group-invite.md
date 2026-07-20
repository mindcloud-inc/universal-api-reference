# Rownd Data Privacy: Delete Group Invite



```
DELETE https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-group-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-group-invite?connectionId=$CONNECTION_ID&group=string&invite=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "string",
  "invite": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/delete-group-invite?${params}`, {
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
| `group` | string | yes | Rownd group identifier. |
| `invite` | string | yes | Rownd group invite identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the invite was deleted. |
| `id` | string | Deleted group invite identifier. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `DELETE /groups/:group/invites/:invite` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group-invite.md) for the provider-specific parameters and requirements.

