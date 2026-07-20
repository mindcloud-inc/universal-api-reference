# Sumsub: Get Applicant Review Status



```
GET https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-review-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-review-status?connectionId=$CONNECTION_ID&applicantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-review-status?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "attemptCnt": 1,
      "attemptId": "string",
      "createDate": "string",
      "levelAutoCheckMode": {},
      "levelName": "Ava Chen",
      "priority": 1,
      "reviewId": "string",
      "reviewStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attemptCnt` | number |  |
| `attemptId` | string |  |
| `createDate` | string |  |
| `levelAutoCheckMode` | object |  |
| `levelName` | string |  |
| `priority` | number |  |
| `reviewId` | string |  |
| `reviewStatus` | string |  |

## Native endpoint

Through the native Sumsub API, this operation is `GET /resources/applicants/:applicantId/status` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicant-review-status.md) for the provider-specific parameters and requirements.

