# Expiration Reminder: Delete Workspace

Deletes a workspace from Expiration Reminder.

```
DELETE https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expiration Reminder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/delete-workspace?${params}`, {
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
      "id": "string",
      "isActive": true,
      "modified": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isActive` | boolean |  |
| `modified` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Expiration Reminder API, this operation is `DELETE /v1/teams/:id` (base URL `https://api.expirationreminder.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workspace.md) for the provider-specific parameters and requirements.

