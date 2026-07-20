# LLMWhisperer: Get Usage Metrics

Retrieves account usage metrics from LLMWhisperer.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-usage-metrics?${params}`, {
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
      "current_page_count": 1,
      "current_page_count_excel": 1,
      "current_page_count_form": 1,
      "current_page_count_high_quality": 1,
      "current_page_count_low_cost": 1,
      "current_page_count_native_text": 1,
      "current_page_count_signature": 1,
      "current_page_count_table": 1,
      "daily_quota": 1,
      "monthly_quota": 1,
      "overage_page_count": 1,
      "subscription_plan": "string",
      "today_page_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page_count` | number |  |
| `current_page_count_excel` | number |  |
| `current_page_count_form` | number |  |
| `current_page_count_high_quality` | number |  |
| `current_page_count_low_cost` | number |  |
| `current_page_count_native_text` | number |  |
| `current_page_count_signature` | number |  |
| `current_page_count_table` | number |  |
| `daily_quota` | number |  |
| `monthly_quota` | number |  |
| `overage_page_count` | number |  |
| `subscription_plan` | string |  |
| `today_page_count` | number |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /get-usage-info` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-metrics.md) for the provider-specific parameters and requirements.

