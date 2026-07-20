# ChipBot: Get Detailed Unique Hits Report



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-unique-hits-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-unique-hits-report?connectionId=$CONNECTION_ID&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/get-detailed-unique-hits-report?${params}`, {
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
| `endDate` | string | yes | The report end date in YYYY-MM-DD format. |
| `startDate` | string | yes | The report start date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Detailed unique-hit rows for the requested range. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v2/connect/accounts/:accountId/domains/:domainId/reporting/analytics/unique-hits/detailed` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-unique-hits-report.md) for the provider-specific parameters and requirements.

