# ClinicalTrials.gov: Get API Version



```
GET https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClinicalTrials.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clinicalTrialsgov/latest/actions/get-api-version?${params}`, {
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
| `format` | string | no | Response format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "dataTimestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string | ClinicalTrials.gov API version. |
| `dataTimestamp` | string | Timestamp of the latest data refresh published by the API. |

## Native endpoint

Through the native ClinicalTrials.gov API, this operation is `GET /version` (base URL `https://clinicaltrials.gov/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-version.md) for the provider-specific parameters and requirements.

