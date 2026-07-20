# Timely: Delete Project

Deletes an existing project from Timely.

```
DELETE https://connect.mindcloud.co/v1/universal/timely/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timely/latest/actions/delete-project?connectionId=$CONNECTION_ID&accountId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/delete-project?${params}`, {
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
| `accountId` | number | yes | Account ID |
| `id` | number | yes | Project ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timely API returns.

## Native endpoint

Through the native Timely API, this operation is `DELETE /1.1/{account_id}/projects/{id}` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

