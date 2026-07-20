# ApptiveGrid: List Access Credentials

Retrieves access credentials from ApptiveGrid.

```
GET https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-access-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ApptiveGrid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-access-credentials?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/list-access-credentials?${params}`, {
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
| `userId` | string | yes | ApptiveGrid user ID. Use the ID returned by Get Current User. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ApptiveGrid API returns.

## Native endpoint

Through the native ApptiveGrid API, this operation is `GET /api/users/:user_id/accessKeys` (base URL `https://app.apptivegrid.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-access-credentials.md) for the provider-specific parameters and requirements.

