# Zixflow: Get List of Activities

Retrieves activities from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-activities?${params}`, {
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
| `filter[]` | array | no | Filter array for activity query. |
| `sort[]` | array | no | Sort instructions for activity query. |
| `limit` | number | no | Maximum number of activities to return. |
| `offset` | number | no | Number of activities to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Activity rows returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the activities query succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `POST /collection-records/activity-list/query` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-of-activities.md) for the provider-specific parameters and requirements.

