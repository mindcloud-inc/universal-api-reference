# CompanyCam: Remove User from Project

Remove an assigned user from a specified Project.

```
DELETE https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/remove-user-from-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/remove-user-from-project?connectionId=$CONNECTION_ID&id=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/remove-user-from-project?${params}`, {
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
| `id` | string | yes | ID of the Project |
| `userId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CompanyCam API returns.

## Native endpoint

Through the native CompanyCam API, this operation is `DELETE projects/:id/assigned_users/:userId` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-project.md) for the provider-specific parameters and requirements.

