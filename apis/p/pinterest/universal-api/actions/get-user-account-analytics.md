# Pinterest: Get User Account Analytics

Retrieves analytics for the current Pinterest user account.

```
GET https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-user-account-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinterest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-user-account-analytics?connectionId=$CONNECTION_ID&startDate=YYYY-MM-DD&endDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "YYYY-MM-DD",
  "endDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinterest/latest/actions/get-user-account-analytics?${params}`, {
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
| `startDate` | string | yes | Example: `YYYY-MM-DD`. |
| `endDate` | string | yes | Example: `YYYY-MM-DD`. |
| `metricTypes` | list<string> | no | One of: `ENGAGEMENT`, `ENGAGEMENT_RATE`, `IMPRESSION`, `OUTBOUND_CLICK`, `OUTBOUND_CLICK_RATE`, `PIN_CLICK`, `PIN_CLICK_RATE`, `SAVE`, `SAVE_RATE`. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinterest API returns.

## Native endpoint

Through the native Pinterest API, this operation is `GET user_account/analytics` (base URL `https://api.pinterest.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-account-analytics.md) for the provider-specific parameters and requirements.

