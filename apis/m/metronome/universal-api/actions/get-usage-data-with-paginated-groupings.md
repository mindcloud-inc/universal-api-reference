# Metronome: Get Usage Data With Paginated Groupings

Retrieves paginated grouped usage data from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-usage-data-with-paginated-groupings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-usage-data-with-paginated-groupings?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=string&billableMetricId=string&windowSize=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "string",
  "billableMetricId": "string",
  "windowSize": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/get-usage-data-with-paginated-groupings?${params}`, {
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
| `customerId` | string | yes | The customer ID. |
| `billableMetricId` | string | yes | The billable metric ID. |
| `windowSize` | string | yes | Aggregation window size. |
| `startingOn` | string | no |  |
| `endingBefore` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ending_before": "2026-05-07T12:00:00.000Z",
      "group_key": "string",
      "group_value": "string",
      "starting_on": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ending_before` | date |  |
| `group_key` | string |  |
| `group_value` | string |  |
| `starting_on` | date |  |
| `value` | number |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/usage/groups` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-usage-data-with-paginated-groupings.md) for the provider-specific parameters and requirements.

