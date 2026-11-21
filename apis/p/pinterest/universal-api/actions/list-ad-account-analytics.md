# Pinterest: List Ad Account Analytics

Retrieves paid ad spend and click metrics for a Pinterest ad account.

```
GET https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-ad-account-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-ad-account-analytics?connectionId=$CONNECTION_ID&adAccountId=string&columns=SPEND_IN_MICRO_DOLLAR%2CCLICKTHROUGH_1&granularity=DAY%2C%20WEEK%2C%20MONTH%2C%20HOUR%20or%20TOTAL&endDate=YYYY-MM-DD&startDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "columns": "SPEND_IN_MICRO_DOLLAR,CLICKTHROUGH_1",
  "granularity": "DAY, WEEK, MONTH, HOUR or TOTAL",
  "endDate": "YYYY-MM-DD",
  "startDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/list-ad-account-analytics?${params}`, {
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
| `adAccountId` | string | yes | Enter the ID of the Pinterest ad account. |
| `columns` | string | yes | Enter comma-separated Pinterest metric names. The defaults are spend in micro-units and clicks on promoted Pins. Use OUTBOUND_CLICK_1 for clicks to a destination outside Pinterest. Default: `SPEND_IN_MICRO_DOLLAR,CLICKTHROUGH_1`. |
| `granularity` | list<string> | yes | Use DAY for daily results. Pinterest also supports TOTAL, HOUR, WEEK, and MONTH. One of: `DAY`, `HOUR`, `MONTH`, `TOTAL`, `WEEK`. Default: `DAY`. Example: `DAY, WEEK, MONTH, HOUR or TOTAL`. |
| `endDate` | string | yes | Example: `YYYY-MM-DD`. |
| `startDate` | string | yes | Example: `YYYY-MM-DD`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `GET ad_accounts/:adAccountId/analytics` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ad-account-analytics.md) for the provider-specific parameters and requirements.

