# Process Plan: Get Total Actual Time Today for Process Instance Tasks for Me



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-total-actual-time-today-for-process-instance-tasks-for-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-total-actual-time-today-for-process-instance-tasks-for-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-total-actual-time-today-for-process-instance-tasks-for-me?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /user/me/process_instance_task/list/today_actual_time/total` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-actual-time-today-for-process-instance-tasks-for-me.md) for the provider-specific parameters and requirements.

