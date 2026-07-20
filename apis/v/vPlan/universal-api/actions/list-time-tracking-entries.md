# vPlan: List Time Tracking Entries



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/list-time-tracking-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/list-time-tracking-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/list-time-tracking-entries?${params}`, {
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
      "count": 1,
      "data": [
        {}
      ],
      "limit": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of returned records. |
| `data` | array<object> | Time tracking records. |
| `limit` | number | Page size limit. |
| `offset` | number | Page offset. |

## Native endpoint

Through the native vPlan API, this operation is `GET /time_tracking` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-tracking-entries.md) for the provider-specific parameters and requirements.

