# HeyPoplar: Create Data Subject Request

Creates a data subject request in HeyPoplar.

```
POST https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-data-subject-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-data-subject-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subjectRequestId": "string",
  "subjectRequestType": "string",
  "submittedTime": "string",
  "subjectIdentities[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/create-data-subject-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subjectRequestId": "string",
    "subjectRequestType": "string",
    "submittedTime": "string",
    "subjectIdentities[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subjectRequestId` | string | yes | Unique UUID v4 identifier for the request. |
| `subjectRequestType` | string | yes | Request type. Supported values: access or erasure. |
| `submittedTime` | string | yes | ISO8601 datetime for when the request was submitted. |
| `subjectIdentities[]` | array<object> | yes | Array of subject identity objects with identity_type, identity_format, and identity_value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "controller_id": "string",
      "encoded_request": "string",
      "expected_completion_time": "string",
      "received_time": "string",
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
| `encoded_request` | string |  |
| `expected_completion_time` | string |  |
| `received_time` | string |  |
| `subject_request_id` | string |  |

## Native endpoint

Through the native HeyPoplar API, this operation is `POST /dsr/request` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-subject-request.md) for the provider-specific parameters and requirements.

