# Jitbit Helpdesk: Get Stats



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-stats?${params}`, {
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
      "closed": 1,
      "handledByMe": 1,
      "inProcess": 1,
      "newTickets": 1,
      "totalTickets": 1,
      "unanswered": 1,
      "unassigned": 1,
      "unclosed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | number | Closed tickets count. |
| `handledByMe` | number | Tickets handled by the authenticated user. |
| `inProcess` | number | In-process tickets count. |
| `newTickets` | number | New tickets count. |
| `totalTickets` | number | Total tickets count. |
| `unanswered` | number | Unanswered tickets count. |
| `unassigned` | number | Unassigned tickets count. |
| `unclosed` | number | Unclosed tickets count. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /Stats` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats.md) for the provider-specific parameters and requirements.

