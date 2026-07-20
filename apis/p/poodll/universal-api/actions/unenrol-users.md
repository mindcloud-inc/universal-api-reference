# Poodll: Unenrol Users

Unenrols users from a Poodll course.

```
DELETE https://connect.mindcloud.co/v1/universal/poodll/latest/actions/unenrol-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/unenrol-users?connectionId=$CONNECTION_ID&enrolments%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "enrolments[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/unenrol-users?${params}`, {
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
| `enrolments[]` | array<object> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Poodll API returns.

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unenrol-users.md) for the provider-specific parameters and requirements.

