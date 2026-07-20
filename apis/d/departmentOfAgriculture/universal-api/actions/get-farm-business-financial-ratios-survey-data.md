# Department of Agriculture: Get Farm Business Financial Ratios Survey Data

Retrieves Farm Business Financial Ratios survey data from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-farm-business-financial-ratios-survey-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-farm-business-financial-ratios-survey-data?connectionId=$CONNECTION_ID&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/get-farm-business-financial-ratios-survey-data?${params}`, {
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
| `variable` | string | no | Optional ARMS variable abbreviation. |
| `state` | string | no | Optional state filter. |
| `farmType` | string | no | Optional farm type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "categoryValue": "string",
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
| `category` | string |  |
| `categoryValue` | string |  |
| `estimate` | number |  |
| `farmType` | string |  |
| `fips_St` | string |  |
| `median` | number |  |
| `report_Num` | number |  |
| `reportName` | string |  |
| `rse` | number |  |
| `stat_Year` | number |  |
| `stateName` | string |  |
| `statistic` | string |  |
| `variableId` | string |  |
| `variableName` | string |  |
| `variableUnit` | string |  |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/surveydata` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-farm-business-financial-ratios-survey-data.md) for the provider-specific parameters and requirements.

