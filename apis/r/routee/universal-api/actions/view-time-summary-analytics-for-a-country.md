# Routee: View Time Summary Analytics for a country

Retrieves time summary analytics for a country from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/view-time-summary-analytics-for-a-country?${params}`, {
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
| `countryCode` | string | yes | The country’s code in ISO 3166­1 alpha­2 format |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `GET /reports/my/breakdown/perCountry` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-time-summary-analytics-for-a-country.md) for the provider-specific parameters and requirements.

