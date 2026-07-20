# Department of Agriculture: Get ARMS Survey Data by Report

Retrieves ARMS survey data by report from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-arms-survey-data-by-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-arms-survey-data-by-report?connectionId=$CONNECTION_ID&year=1&report=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "1",
  "report": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-arms-survey-data-by-report?${params}`, {
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
| `year` | number | yes | ARMS survey year. |
| `report` | string | yes | ARMS report number or report name. |
| `variable` | string | no | Optional ARMS variable abbreviation such as `kount`. |
| `state` | string | no | Optional state code/name; provider defaults to all survey states. |
| `farmType` | string | no | Optional farm type filter. |
| `category` | string | no | Optional primary category. |
| `categoryValue` | string | no | Optional primary category value. |
| `category2` | string | no | Optional secondary category. |
| `category2Value` | string | no | Optional secondary category value. |
| `subReport` | number | no | Optional ARMS sub-report ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "category2": "string",
      "category2Value": "string",
      "categoryValue": "string",
      "dec_Disp": 1,
      "estimate": 1,
      "farmType": "string",
      "fips_St": "string",
      "median": 1,
      "report_Num": 1,
      "reportName": "Ava Chen",
      "rse": 1,
      "stat_Year": 1,
      "stateName": "Ava Chen",
      "statistic": "string",
      "unreliable_Est": 1,
      "variableId": "string",
      "variableName": "Ava Chen",
      "variableUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Primary category. |
| `category2` | string | Secondary category. |
| `category2Value` | string | Secondary category value. |
| `categoryValue` | string | Primary category value. |
| `dec_Disp` | number | Decimal display precision. |
| `estimate` | number | Estimated value. |
| `farmType` | string | Farm type. |
| `fips_St` | string | State FIPS code. |
| `median` | number | Median value, when supplied. |
| `report_Num` | number | Report number. |
| `reportName` | string | Report name. |
| `rse` | number | Relative standard error. |
| `stat_Year` | number | Survey year. |
| `stateName` | string | State name. |
| `statistic` | string | Statistic label. |
| `unreliable_Est` | number | Provider unreliable-estimate flag. |
| `variableId` | string | Variable abbreviation. |
| `variableName` | string | Variable display name. |
| `variableUnit` | string | Variable unit. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/surveydata` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-arms-survey-data-by-report.md) for the provider-specific parameters and requirements.

