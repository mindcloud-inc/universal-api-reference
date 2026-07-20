# Captain Data: Get Quotas

Retrieves workspace quota details from Captain Data.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/get-quotas?${params}`, {
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
      "credits_left": 1,
      "credits_max": 1,
      "credits_used": 1,
      "current_month_end": "string",
      "current_month_start": "string",
      "name": "Ava Chen",
      "plan_name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_left` | number |  |
| `credits_max` | number |  |
| `credits_used` | number |  |
| `current_month_end` | string |  |
| `current_month_start` | string |  |
| `name` | string |  |
| `plan_name` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /quotas` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotas.md) for the provider-specific parameters and requirements.

