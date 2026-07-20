# Routee: View Time Summary Analytics for a country and a network

Retrieves time summary analytics for a country and a network from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country-and-a-network
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country-and-a-network?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&mcc=string&mnc=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "mcc": "string",
  "mnc": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country-and-a-network?${params}`, {
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
| `startDate` | date | yes | starting date to get reports |
| `endDate` | date | yes | ending date to get reports |
| `mcc` | string | yes | the mcc code |
| `mnc` | string | yes | the mnc code |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/breakdown/perMccMnc` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-time-summary-analytics-for-a-country-and-a-network.md) for the provider-specific parameters and requirements.

