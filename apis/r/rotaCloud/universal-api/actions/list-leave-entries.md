# RotaCloud: List Leave Entries

Lists leave records in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-entries?${params}`, {
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
      "admin": 1,
      "admin_message": "string",
      "dates": [
        {}
      ],
      "deleted": true,
      "end_date": "string",
      "hours": {},
      "id": 1,
      "paid": true,
      "replied_at": 1,
      "requested": true,
      "requested_at": 1,
      "start_date": "string",
      "status": "string",
      "type": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | number |  |
| `admin_message` | string |  |
| `dates` | array<object> |  |
| `deleted` | boolean |  |
| `end_date` | string |  |
| `hours` | object |  |
| `id` | number |  |
| `paid` | boolean |  |
| `replied_at` | number |  |
| `requested` | boolean |  |
| `requested_at` | number |  |
| `start_date` | string |  |
| `status` | string |  |
| `type` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/leave` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-entries.md) for the provider-specific parameters and requirements.

