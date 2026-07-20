# Sumsub: Get Applicant-Facing Consents



```
GET https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-facing-consents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-facing-consents?connectionId=$CONNECTION_ID&applicantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-facing-consents?${params}`, {
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
| `applicantId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumsub API returns.

## Native endpoint

Through the native Sumsub API, this operation is `GET /resources/applicants/:applicantId/acceptedAgreements` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicant-facing-consents.md) for the provider-specific parameters and requirements.

