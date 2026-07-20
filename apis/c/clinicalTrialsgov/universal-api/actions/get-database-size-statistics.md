# ClinicalTrials.gov: Get Database Size Statistics



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-database-size-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-database-size-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-database-size-statistics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "averageSizeBytes": 1,
      "largestStudies": [
        {}
      ],
      "percentiles": {},
      "ranges": [
        {}
      ],
      "totalStudies": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageSizeBytes` | number | Average study record size in bytes. |
| `largestStudies` | array<object> | Largest study records in the database. |
| `percentiles` | object | Record size percentile summary. |
| `ranges` | array<object> | Distribution of study sizes by range. |
| `totalStudies` | number | Total number of studies in the database. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /stats/size` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-size-statistics.md) for the provider-specific parameters and requirements.

