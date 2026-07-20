# Refiner: Get Reporting

Retrieves survey reporting data from Refiner.

```
GET https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-reporting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-reporting?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-reporting?${params}`, {
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
| `type` | string | yes | The reporting type: nps, csat, ratings, distribution, or count. |
| `questionIdentifiers[]` | array<string> | no | Only include matching question identifiers in the report. |
| `tagUuids[]` | array<string> | no | Only include responses tagged with these tag UUIDs. |
| `formUuids[]` | array<string> | no | Only include the selected form UUIDs. |
| `segmentUuids[]` | array<string> | no | Only include the selected segment UUIDs. |
| `dateRangeStart` | date | no | Only count data points recorded after this time. |
| `dateRangeEnd` | date | no | Only count data points recorded before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "average": 1,
      "count": 1,
      "csat": 1,
      "data": {},
      "datapoints": 1,
      "dateRangeEnd": "2026-05-07T12:00:00.000Z",
      "dateRangeStart": "2026-05-07T12:00:00.000Z",
      "nps": 1,
      "responses": 1,
      "sum": 1,
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `average` | number |  |
| `count` | number |  |
| `csat` | number |  |
| `data` | object |  |
| `datapoints` | number |  |
| `dateRangeEnd` | date |  |
| `dateRangeStart` | date |  |
| `nps` | number |  |
| `responses` | number |  |
| `sum` | number |  |
| `views` | number |  |

## Native endpoint

Through the native Refiner API, this operation is `GET /reporting` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reporting.md) for the provider-specific parameters and requirements.

