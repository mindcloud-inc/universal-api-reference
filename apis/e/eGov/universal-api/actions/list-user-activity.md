# e-Gov: List User Activity

Retrieves user activity from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-user-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-user-activity?connectionId=$CONNECTION_ID&limit=25&offset=0&id=35ba0c6e-0ae3-406e-b5f8-105c37bd5abf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "35ba0c6e-0ae3-406e-b5f8-105c37bd5abf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-user-activity?${params}`, {
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
| `id` | string | yes | Default: `35ba0c6e-0ae3-406e-b5f8-105c37bd5abf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity_type": "string",
      "data": {},
      "id": "string",
      "object_id": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_type` | string |  |
| `data` | object |  |
| `id` | string |  |
| `object_id` | string |  |
| `timestamp` | date |  |
| `user_id` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /user_activity_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-activity.md) for the provider-specific parameters and requirements.

