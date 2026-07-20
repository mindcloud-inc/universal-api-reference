# Codeberg: List User Tracked Times



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-tracked-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-tracked-times?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-user-tracked-times?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "issue_id": 1,
      "issue": {
        "number": 1,
        "state": "string",
        "title": "string"
      },
      "time": 1,
      "user_id": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | number |  |
| `issue_id` | number |  |
| `issue.number` | number |  |
| `issue.state` | string |  |
| `issue.title` | string |  |
| `time` | number |  |
| `user_id` | number |  |
| `user_name` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/times` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-tracked-times.md) for the provider-specific parameters and requirements.

