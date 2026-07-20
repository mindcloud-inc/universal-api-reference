# ClinicalTrials.gov: Get Field Value Statistics



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-field-value-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-field-value-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-field-value-statistics?${params}`, {
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
| `fields` | string | no | One or more data fields or pieces to analyze. |
| `types` | string | no | Optional field types to restrict the statistics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": "string",
      "missingStudiesCount": 1,
      "piece": "string",
      "topValues": [
        {}
      ],
      "type": "string",
      "uniqueValuesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | string | JSON field path analyzed. |
| `missingStudiesCount` | number | Number of studies missing the requested field. |
| `piece` | string | ClinicalTrials.gov piece name analyzed. |
| `topValues` | array<object> | Most common observed values. |
| `type` | string | Statistic type for the requested field. |
| `uniqueValuesCount` | number | Number of distinct values found. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /stats/field/values` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field-value-statistics.md) for the provider-specific parameters and requirements.

