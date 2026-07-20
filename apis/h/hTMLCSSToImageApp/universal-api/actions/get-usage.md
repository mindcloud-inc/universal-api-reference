# HTML/CSS to Image app: Get Usage



```
GET https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage?${params}`, {
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
      "data": {
        "day": {
          "value20260313T000000Z": 1
        },
        "hour": {
          "value20260313T150000Z": 1,
          "value20260313T160000Z": 1
        },
        "month": {
          "value20260301T000000Z": 1
        }
      },
      "perBillingPeriod": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.day` | object |  |
| `data.day.value20260313T000000Z` | number |  |
| `data.hour` | object |  |
| `data.hour.value20260313T150000Z` | number |  |
| `data.hour.value20260313T160000Z` | number |  |
| `data.month` | object |  |
| `data.month.value20260301T000000Z` | number |  |
| `perBillingPeriod[]` | array<object> |  |
| `perBillingPeriod[].end` | string |  |
| `perBillingPeriod[].start` | string |  |
| `perBillingPeriod[].totalImages` | number |  |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `GET /v1/usage` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

