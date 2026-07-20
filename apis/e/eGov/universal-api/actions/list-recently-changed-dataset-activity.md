# e-Gov: List Recently Changed Dataset Activity

Retrieves recently changed dataset activity from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-recently-changed-dataset-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-recently-changed-dataset-activity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-recently-changed-dataset-activity?${params}`, {
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

Through the native e-Gov API, this operation is `GET /recently_changed_packages_activity_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-recently-changed-dataset-activity.md) for the provider-specific parameters and requirements.

