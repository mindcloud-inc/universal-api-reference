# ClinicalTrials.gov: Get Study



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study?connectionId=$CONNECTION_ID&nctId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nctId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-study?${params}`, {
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
| `fields` | string | no | Return only selected fields. |
| `nctId` | string | yes | ClinicalTrials.gov study identifier such as NCT06100835. |
| `markupFormat` | string | no | Preferred format for markup fields. One of: `0`, `1`. |
| `format` | string | no | Response format. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "derivedSection": {},
      "hasResults": true,
      "protocolSection": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `derivedSection` | object | Derived browse and metadata fields. |
| `hasResults` | boolean | Whether the study has posted results. |
| `protocolSection` | object | Primary protocol details for the study. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /studies/:nctId` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-study.md) for the provider-specific parameters and requirements.

