# Zillow Econ: Get market report

Retrieves market report data from Zillow Econ.

```
GET https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Econ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-report?connectionId=$CONNECTION_ID&stateCodeFIPS=48" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stateCodeFIPS": "48"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowEcon/latest/actions/get-market-report?${params}`, {
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
| `stateCodeFIPS` | string | yes | Two-digit state FIPS code for the market report region. Default: `48`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": "2026-05-07T12:00:00.000Z",
      "cutTypeKey": "string",
      "dataValue": 1,
      "id": 1,
      "metricTypeKey": "string",
      "municipalCodeFIPS": "string",
      "region": "string",
      "regionCity": "string",
      "regionCounty": "string",
      "regionID": 1,
      "regionMetro": "string",
      "regionState": "string",
      "regionType": "string",
      "regionTypeID": 1,
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "stateCodeFIPS": "string",
      "timePeriodEndDateTime": "2026-05-07T12:00:00.000Z",
      "timePeriodTypeKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date | Date the metric was created. |
| `cutTypeKey` | string | Unique key indicating the cut combination for this record. |
| `dataValue` | number | Metric value. |
| `id` | number | Unique identifier of the imported record. |
| `metricTypeKey` | string | Unique key for the metric type. |
| `municipalCodeFIPS` | string | Three-digit FIPS municipal code. |
| `region` | string | Region name. |
| `regionCity` | string | City containing the region. |
| `regionCounty` | string | County containing the region. |
| `regionID` | number | Unique region identifier. |
| `regionMetro` | string | Metro containing the region. |
| `regionState` | string | State containing the region. |
| `regionType` | string | Region type. |
| `regionTypeID` | number | Unique identifier of the region type. |
| `releaseDate` | date | Date the metric was released. |
| `stateCodeFIPS` | string | Two-digit FIPS state code. |
| `timePeriodEndDateTime` | date | End timestamp of the metric reporting window. |
| `timePeriodTypeKey` | string | Time window over which the metric is calculated. |

## Native endpoint

Through the native Zillow Econ API, this operation is `GET /zgecon/marketreport` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-market-report.md) for the provider-specific parameters and requirements.

