# Bureau of Labor Statistics: Get Survey

Retrieves metadata for a Bureau of Labor Statistics survey.

```
GET https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bureau of Labor Statistics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyAbbreviation=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyAbbreviation": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bureauOfLaborStatistics/latest/actions/get-survey?${params}`, {
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
| `surveyAbbreviation` | string | yes | BLS survey abbreviation, for example TU. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": [
        "string"
      ],
      "responseTime": 1,
      "Results": {
        "survey": [
          {
            "allowsNetChange": "string",
            "allowsPercentChange": "string",
            "hasAnnualAverages": "string",
            "survey_abbreviation": "string",
            "survey_name": "Ava Chen"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | array<string> | BLS response messages. |
| `responseTime` | number | BLS response time in milliseconds. |
| `Results` | object | BLS response results envelope. |
| `Results.survey` | array<object> | Requested BLS survey metadata. |
| `Results.survey[].allowsNetChange` | string | Whether net change calculations are allowed. |
| `Results.survey[].allowsPercentChange` | string | Whether percent change calculations are allowed. |
| `Results.survey[].hasAnnualAverages` | string | Whether annual averages are available. |
| `Results.survey[].survey_abbreviation` | string | Survey abbreviation. |
| `Results.survey[].survey_name` | string | Survey name. |
| `status` | string | BLS request status returned by runtime. |

## Native endpoint

Through the native Bureau of Labor Statistics API, this operation is `GET /surveys/:surveyAbbreviation` (base URL `https://api.bls.gov/publicAPI/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

