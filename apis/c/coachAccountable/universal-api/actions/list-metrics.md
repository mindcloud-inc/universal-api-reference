# CoachAccountable: List Metrics

Retrieves metrics from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-metrics?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-metrics?${params}`, {
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
| `clientId` | number | yes | The Client whose Metrics are to be gotten. |
| `includeCompleted` | boolean | no | Set to true to include Metrics that have already been marked complete, otherwise complete Metrics will be omitted. Default: `false`. |
| `includeData` | boolean | no | Set to false in order to omit dataSet from the return value. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataMode": "string",
      "dataSet": [
        {
          "comment": "string",
          "dateOf": "2026-05-07T12:00:00.000Z",
          "value": 1
        }
      ],
      "endDate": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "name": "Ava Chen",
      "repeatRule": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "targetEnd": 1,
      "targetMode": "string",
      "targetStart": 1,
      "totalWeight": 1,
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataMode` | string |  |
| `dataSet` | array<object> |  |
| `dataSet[].comment` | string |  |
| `dataSet[].dateOf` | date |  |
| `dataSet[].value` | number |  |
| `endDate` | date |  |
| `ID` | number |  |
| `name` | string |  |
| `repeatRule` | string |  |
| `startDate` | date |  |
| `targetEnd` | number |  |
| `targetMode` | string |  |
| `targetStart` | number |  |
| `totalWeight` | number |  |
| `units` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-metrics.md) for the provider-specific parameters and requirements.

