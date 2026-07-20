# ClinicalTrials.gov: Get Study FHIR JSON



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study-fhir-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study-fhir-json?connectionId=$CONNECTION_ID&nctId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nctId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study-fhir-json?${params}`, {
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
| `nctId` | string | yes | ClinicalTrials.gov study identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": [
        {}
      ],
      "resourceType": "string",
      "timestamp": "string",
      "total": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry` | array<object> | FHIR bundle entries returned for the study. |
| `resourceType` | string | FHIR resource bundle type. |
| `timestamp` | string | Bundle generation timestamp. |
| `total` | number | Number of entries in the bundle. |
| `type` | string | FHIR bundle subtype. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies/:nctId` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-study-fhir-json.md) for the provider-specific parameters and requirements.

