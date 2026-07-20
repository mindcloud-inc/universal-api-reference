# Communi App: Get User Group



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-group?connectionId=$CONNECTION_ID&id=343753-88729" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "343753-88729"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/get-user-group?${params}`, {
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
| `id` | string | yes | Default: `343753-88729`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "group": 1,
      "id": "string",
      "roleId": 1,
      "status": 1,
      "statusChangedBy": 1,
      "statusChangedOn": "2026-05-07T12:00:00.000Z",
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `createdOn` | date |  |
| `group` | number |  |
| `id` | string |  |
| `roleId` | number |  |
| `status` | number |  |
| `statusChangedBy` | number |  |
| `statusChangedOn` | date |  |
| `user` | number |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/userGroup/:id` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-group.md) for the provider-specific parameters and requirements.

