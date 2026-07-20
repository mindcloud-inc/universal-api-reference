# EndBounce: Get Verification Job Results

Retrieves verification job results from EndBounce.

```
GET https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EndBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-results?connectionId=$CONNECTION_ID&request_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/get-verification-job-results?${params}`, {
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
| `request_id` | string | yes | Verification job request ID. |
| `status` | string | no | Filter results by verification status. Default: `all`. |
| `offset` | number | no | Row offset for paginating job results. Default: `0`. |
| `limit` | number | no | Maximum number of result rows to return. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "partial": true,
      "rows": [
        {
          "email": "ava@example.com",
          "isCatchAll": 1,
          "isDisposable": 1,
          "isRole": 1,
          "reason": "string",
          "score": 1,
          "status": "string",
          "verifiedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partial` | boolean | Whether the response is partial. |
| `rows` | array<object> | Verification result rows. |
| `rows[].email` | string | Verified email address. |
| `rows[].isCatchAll` | number | Catch-all flag returned as 0 or 1. |
| `rows[].isDisposable` | number | Disposable flag returned as 0 or 1. |
| `rows[].isRole` | number | Role-address flag returned as 0 or 1. |
| `rows[].reason` | string | Verification reason code. |
| `rows[].score` | number | Verification confidence score. |
| `rows[].status` | string | Verification status. |
| `rows[].verifiedAt` | date | When the row was verified. |
| `total` | number | Total rows returned or available for the query. |

## Native endpoint

Through the native EndBounce API, this operation is `GET /v1/jobs/:request_id/results` (base URL `https://api.endbounce.com/api/integrations`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-job-results.md) for the provider-specific parameters and requirements.

