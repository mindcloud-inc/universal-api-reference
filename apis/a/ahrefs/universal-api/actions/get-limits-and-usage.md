# Ahrefs: Get Limits And Usage



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-limits-and-usage?${params}`, {
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
      "limits_and_usage": {
        "api_key_expiration_date": "2026-05-07T12:00:00.000Z",
        "subscription": "string",
        "units_limit_api_key": 1,
        "units_limit_workspace": 1,
        "units_usage_api_key": 1,
        "units_usage_workspace": 1,
        "usage_reset_date": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limits_and_usage` | object | Subscription limits and usage object. |
| `limits_and_usage.api_key_expiration_date` | date |  |
| `limits_and_usage.subscription` | string |  |
| `limits_and_usage.units_limit_api_key` | number |  |
| `limits_and_usage.units_limit_workspace` | number |  |
| `limits_and_usage.units_usage_api_key` | number |  |
| `limits_and_usage.units_usage_workspace` | number |  |
| `limits_and_usage.usage_reset_date` | date |  |

## Native endpoint

Through the native Ahrefs API, this operation is `GET /subscription-info/limits-and-usage` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-limits-and-usage.md) for the provider-specific parameters and requirements.

