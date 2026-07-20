# Instantly: Get Daily Account Analytics

Retrieves daily account analytics from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-account-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-account-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-daily-account-analytics?${params}`, {
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
| `startDate` | date | no | Start date for the analytics period, YYYY-MM-DD. |
| `endDate` | date | no | End date for the analytics period, YYYY-MM-DD. |
| `emails[]` | array<string> | no | Email accounts to filter by. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounced": 1,
      "date": "string",
      "email_account": "ava@example.com",
      "sent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | number | Bounced count. |
| `date` | string | Analytics date. |
| `email_account` | string | Email account. |
| `sent` | number | Sent count. |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/accounts/analytics/daily` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-account-analytics.md) for the provider-specific parameters and requirements.

