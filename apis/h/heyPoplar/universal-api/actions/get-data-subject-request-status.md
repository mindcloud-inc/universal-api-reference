# HeyPoplar: Get Data Subject Request Status

Retrieves a data subject request status from HeyPoplar.

```
GET https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-data-subject-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-data-subject-request-status?connectionId=$CONNECTION_ID&subjectRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subjectRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-data-subject-request-status?${params}`, {
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
| `subjectRequestId` | string | yes | The subject_request_id returned by the create request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "controller_id": "string",
      "expected_completion_time": "string",
      "request_status": "string",
      "subject_request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `controller_id` | string |  |
| `expected_completion_time` | string |  |
| `request_status` | string |  |
| `subject_request_id` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `GET /dsr/request/:subject_request_id` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-subject-request-status.md) for the provider-specific parameters and requirements.

