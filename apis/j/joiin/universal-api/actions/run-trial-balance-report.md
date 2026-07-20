# Joiin: Run Trial Balance Report

Retrieves a trial balance report from Joiin.

```
GET https://connect.mindcloud.co/v1/universal/joiin/latest/actions/run-trial-balance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joiin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joiin/latest/actions/run-trial-balance-report?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&currency=string&companies%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "currency": "string",
  "companies[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joiin/latest/actions/run-trial-balance-report?${params}`, {
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
| `startDate` | date | yes | The report start date in YYYY-MM format. |
| `endDate` | date | yes | The report end date in YYYY-MM format. |
| `currency` | string | yes | The report currency code, for example USD. |
| `companies[]` | array<string> | yes | A list of company IDs or company names to include in the report. |
| `eliminationSet` | string | no | The elimination set to use for the report. |
| `eliminationType` | string | no | How Joiin should apply eliminations for the report. |
| `periodNumber` | number | no | The period number to use for the trial balance report. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "companies": [
        {}
      ],
      "currency": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "headers": [
        {}
      ],
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | The trial balance accounts returned by Joiin. |
| `companies` | array<object> | The companies included in the report. |
| `currency` | string | The report currency. |
| `endDate` | date | The report end date. |
| `headers` | array<object> | Column headers describing the returned values. |
| `startDate` | date | The report start date. |

## Native endpoint

Through the native Joiin API, this operation is `POST /v1/report/trial-balance` (base URL `https://app-api.joiin.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-trial-balance-report.md) for the provider-specific parameters and requirements.

