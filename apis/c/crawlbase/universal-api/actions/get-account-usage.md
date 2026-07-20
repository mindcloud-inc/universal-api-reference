# Crawlbase: Get Account Usage

Retrieves account usage statistics from Crawlbase.

```
GET https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-account-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crawlbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-account-usage?connectionId=$CONNECTION_ID&product=crawling-api" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "product": "crawling-api"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-account-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product` | list | yes | Crawlbase product to report usage for. One of: `0`, `1`, `2`, `3`, `4`, `5`. Default: `crawling-api`. |
| `previousMonth` | boolean | no | Set true to include current and previous month statistics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domainStats": [
        {}
      ],
      "remainingCredits": 1,
      "totalDue": 1,
      "totalFailed": 1,
      "totalSuccess": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domainStats` | array<object> | Usage summary by domain. |
| `remainingCredits` | number | Remaining subscription credits when applicable. |
| `totalDue` | number | Amount due in USD for successful requests. |
| `totalFailed` | number | Failed requests in the current month. |
| `totalSuccess` | number | Successful requests in the current month. |

## Native endpoint

Through the native Crawlbase API, this operation is `GET /account` (base URL `https://api.crawlbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-usage.md) for the provider-specific parameters and requirements.

