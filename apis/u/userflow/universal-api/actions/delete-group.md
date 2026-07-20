# Userflow: Delete Group

Deletes an existing group from Userflow.

```
DELETE https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/delete-group?${params}`, {
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
| `groupId` | string | yes | The Userflow group ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the group was deleted. |
| `id` | string | Deleted group ID. |
| `object` | string | Returned object type. |

## Native endpoint

Through the native Userflow API, this operation is `DELETE /groups/:group_id` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-group.md) for the provider-specific parameters and requirements.

