# Reverse Contact: Get Usage



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/get-usage?${params}`, {
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
      "creditsConsumed": 1,
      "key": {
        "dailyLimit": 1,
        "id": "string",
        "minuteRateLimit": {
          "left": 1,
          "limit": 1,
          "nextReset": "2026-05-07T12:00:00.000Z",
          "used": 1
        }
      },
      "workspace": {
        "allowDailyOvercost": true,
        "credits": {
          "left": 1,
          "total": 1,
          "used": 1
        },
        "dailyLimit": 1,
        "hasUnlimitedCredits": true,
        "id": "string",
        "minuteRateLimit": {
          "left": 1,
          "limit": 1,
          "nextReset": "2026-05-07T12:00:00.000Z",
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
| `creditsConsumed` | number |  |
| `key.dailyLimit` | number |  |
| `key.id` | string |  |
| `key.minuteRateLimit.left` | number |  |
| `key.minuteRateLimit.limit` | number |  |
| `key.minuteRateLimit.nextReset` | date |  |
| `key.minuteRateLimit.used` | number |  |
| `workspace.allowDailyOvercost` | boolean |  |
| `workspace.credits.left` | number |  |
| `workspace.credits.total` | number |  |
| `workspace.credits.used` | number |  |
| `workspace.dailyLimit` | number |  |
| `workspace.hasUnlimitedCredits` | boolean |  |
| `workspace.id` | string |  |
| `workspace.minuteRateLimit.left` | number |  |
| `workspace.minuteRateLimit.limit` | number |  |
| `workspace.minuteRateLimit.nextReset` | date |  |
| `workspace.minuteRateLimit.used` | number |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `GET /v2/usage` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

