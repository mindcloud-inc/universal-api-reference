# VatcheckAPI: Check Status

Retrieves the current quota status from VatcheckAPI.

```
GET https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VatcheckAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/check-status?${params}`, {
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
      "account_id": 1,
      "quotas": {
        "grace": {
          "remaining": 1,
          "total": 1,
          "used": 1
        },
        "month": {
          "remaining": 1,
          "total": 1,
          "used": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number | VatcheckAPI account identifier for the current API key. |
| `quotas` | object | Quota information grouped by period. |
| `quotas.grace` | object | Grace quota information. |
| `quotas.grace.remaining` | number | Remaining grace quota calls. |
| `quotas.grace.total` | number | Total grace quota calls. |
| `quotas.grace.used` | number | Used grace quota calls. |
| `quotas.month` | object | Monthly quota information. |
| `quotas.month.remaining` | number | Remaining calls in the month. |
| `quotas.month.total` | number | Total available calls in the month. |
| `quotas.month.used` | number | Used calls in the month. |

## Native endpoint

Through the native VatcheckAPI API, this operation is `GET /v2/status` (base URL `https://api.vatcheckapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-status.md) for the provider-specific parameters and requirements.

