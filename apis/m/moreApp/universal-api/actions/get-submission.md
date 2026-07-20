# MoreApp: Get Submission

Retrieves a submission from MoreApp.

```
GET https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-submission?connectionId=$CONNECTION_ID&customerId=209321&submissionId=000000000000000000000000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "submissionId": "000000000000000000000000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/get-submission?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `submissionId` | string | yes | MoreApp submission identifier. Default: `000000000000000000000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "scope": "string",
      "status": 1,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object | Additional provider error details when present. |
| `message` | string | Provider message describing the submission lookup result. |
| `scope` | string | MoreApp error scope for the submission response. |
| `status` | number | HTTP-style provider status returned when the submission id is not found. |
| `traceId` | string | MoreApp trace identifier for support and debugging. |

## Native endpoint

Through the native MoreApp API, this operation is `GET /api/v1.0/customers/{{customerId}}/submissions/{{submissionId}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

