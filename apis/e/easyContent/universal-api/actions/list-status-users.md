# EasyContent: List Status Users

Retrieves users assignable to a selected EasyContent workflow status.

```
GET https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-status-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyContent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-status-users?connectionId=$CONNECTION_ID&projectId=1&statusId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "statusId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/list-status-users?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |
| `projectId` | number | yes |  |
| `statusId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyContent API returns.

## Native endpoint

Through the native EasyContent API, this operation is `GET /zapier/resources/users-that-can-be-assigned-to-status` (base URL `https://easycontent.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-status-users.md) for the provider-specific parameters and requirements.

