# Nyne AI: Get API Usage

Retrieves API usage details from Nyne AI.

```
GET https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyne AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage?${params}`, {
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
      "breakdown": {},
      "credits_by_api": {},
      "limits": {},
      "month": 1,
      "period": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breakdown` | object | Credit consumption breakdown. |
| `credits_by_api` | object | Credit usage grouped by API. |
| `limits` | object | Credit limit details. |
| `month` | number | Usage month. |
| `period` | string | Usage period. |
| `success` | boolean | Whether the usage request succeeded. |
| `timestamp` | date | Response timestamp. |
| `year` | number | Usage year. |

## Native endpoint

Through the native Nyne AI API, this operation is `GET /usage` (base URL `https://api.nyne.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage.md) for the provider-specific parameters and requirements.

