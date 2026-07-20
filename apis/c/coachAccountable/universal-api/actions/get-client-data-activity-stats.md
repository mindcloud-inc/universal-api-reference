# CoachAccountable: Get Client Data Activity Stats

Retrieves client activity stats from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-activity-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-activity-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-data-activity-stats?${params}`, {
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
| `clientId` | number | no | The ID of the client for whom data is to be returned, if desired only for a single, specific client. |
| `groupId` | number | no | The ID of the Group for whose client members data is to be returned. |
| `companyId` | number | no | The ID of the Company for whose client members data is to be returned. |
| `engagementId` | number | no | The ID of the Engagement for whose client data is to be returned. |
| `dateBucket` | list | no | Group activity statistics according to your bucket size of choice. One of: `D`, `M`, `Q`, `W`, `Y`. Default: `W`. |
| `dateFrom` | date | no | The lower bound of the date range to report stats on.. |
| `dateTo` | date | no | The upper bound of the date range to report stats on. |
| `itemTypes` | string | no | The types of items to be included, each letter signifies a single type. A for Action, M for Metric, P for Appointment, S for Session Note, W for Worksheet, J for Journal Entry, F for File, C for Comment. |
| `includeInactive` | boolean | no | Include data for Clients who are inactive. Default: `false`. |
| `includeTotals` | boolean | no | Set true to inclue a totals column. Default: `true`. |
| `includeAverages` | boolean | no | Set true to inclue an averages column. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-data-activity-stats.md) for the provider-specific parameters and requirements.

